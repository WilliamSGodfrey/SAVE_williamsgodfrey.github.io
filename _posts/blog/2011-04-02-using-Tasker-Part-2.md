---
id: 70
title: 'Using Tasker to Record the Location of an Android Device [Part 2]'
date: 2011-04-02T18:54:38+00:00
layout: post
permalink: /using-tasker-to-record-the-location-an-android-device-part-2/
dsq_thread_id:
  - 2021358279
categories:
  - Tasker
tags:
  - Android
  - Droid X
  - GPS
  - Location
  - Stolen Phone
  - Tasker
excerpt: ""
---

_[This is Part 2 of a 2 part series discussing the use of the Tasker application to record the location of a device running Google's Android mobile OS. This part discusses how to set up the Tasker profile and my first impressions [Part 1](http://www.williamsgodfrey.com/using-tasker-to-record-the-location-an-android-device-part-1/) discusses what lead me to use the Tasker application.]_

In the writeup that follows, I assume that the reader is familiar with the [Tasker for Android](http://tasker.dinglisch.net/) application. If something doesn't seem to make sense, please feel free to leave a comment or contact me via Twitter or email.

### Setting Up the Profile in Tasker

* Begin by setting up a new profile, I named mine "Tweet Loca."

* We want the profile to run continuously in the background whenever the phone is on. Therefore, we want a time context so after naming the profile we will select **Time** from the 'First Context' menu that pops up. As shown in the figure, I used the current time for the 'From:' time and one minute _before_ the current time for the 'To:' time. I also set the profile to repeat every 15 minutes in the 'Repeat:' section. 

<figure>
  <img src="{{ site.url }}/images/firstcontexttime.png" >
  <figcaption>Setting the profile to run continuously.</figcaption>
</figure>

### Defining the Actions in Tasker (aka Tasks)

* The first task to be run will update the value currently stored in the Tasker variable `%LOC` if the most recent GPS fix occurred more than 15 minutes prior. This is done because I found that often the phone has not had a reason to find its GPS position recently, making any current values stored in `%LOC` outdated and useless. So for the first Task, first select **Misc** from the 'Select Action Category' menu and then **Get Location** from the 'Select Misc Action' menu. For 'Source' we will select GPS, and we'll check the 'If' box and enter `%GPS_AGE` and `5` in the 'If' input boxes. See the image. Don't worry about the `%GPS_AGE` variable, we'll define it soon enough. 

<figure>
  <img src="{{ site.url }}/images/firsttasklocation.png" >
  <figcaption>Defining variables.</figcaption>
</figure>
      
* The next few Tasks will define the variables we'll need for the profile to properly report the locations of the phone. Add another Task (push the '+' button in the lower left corner of the profile window), select **Variable** from the 'Select Action Category' menu  and then **Variable Set** from the 'Select Variable Action' menu. For 'Name,' enter `%GPS_AGE_SEC`, for 'To,' enter `%TIMES – %LOCTMS`, and check the 'Do Maths' box. This defines a variable for the time since the last GPS fix in seconds, `%GPS_AGE_SEC`, as the time of the last GPS fix in seconds, `%LOCTMS`, subtracted from the current time in seconds, `%TIMES`.

<figure>
  <img src="{{ site.url }}/images/GPSAGEdefine.png" >
  <figcaption>Defining more variables.</figcaption>
</figure>
      
* Select **Variable Set** again. This time for 'Name,' enter `%GPS_AGE`, for 'To,' enter `%GPS_AGE_SEC / 60`, and check the 'Do Maths' box. This converts `%GPS_AGE_SEC` to units of minutes, which is what we'll use to report the GPS fix age.
* Select **Variable Set** again. This time for 'Name,' enter `%NET_AGE_SEC`, for 'To,' enter `%TIMES - %LOCNTMS`, and check the 'Do Maths' box. This defines a variable for the time since the last wifi location fix in seconds, `%NET_AGE_SEC`, as the time of the last wifi fix in seconds, `%LOCNTMS`, subtracted from the current time in seconds, `%TIMES`. We do this because we'lll report our net location as well, as a backup to determine the reliability of our GPS data. 
* Select **Variable Set** again. This time for 'Name,' enter `%NET_AGE`, for 'To,' enter `%NET_AGE_SEC / 60`, and check the 'Do Maths' box. This converts `%NET_AGE_SEC` to units of minutes, which is what we'll use to report the wifi location fix age
* Select **Variable Set** again. This time for 'Name,' enter `%LOCACC_FT`, for 'To,' enter `%LOCACC * 3.281`, and check the 'Do Maths' box. This defines a variable used to store the accuracy of the last GPS fix in feet, `%LOCACC_FT`, by converting the built in Tasker variable, `%LOCACC`, from units of meters to units of feet.
* Select **Variable Set** again (last variable!). This time for 'Name,' enter `%LOCNACC_FT`, for 'To,' enter `%LOCNACC * 3.281`, and check the 'Do Maths' box. This defines a variable used to store the accuracy of the last wifi location fix in feet, `%LOCNACC_FT`, by converting the built-in Tasker variable, `%LOCNACC`, from units of meters to units of feet.
All our variables are now set up and the only thing left to do is report them. I found having the phone automatically tweet it's location to [a 'locked' Twitter account](http://twitter.com/#!/wsglocation) works best for me. I was originally storing the phone's location to a local text file but, after leaving my phone at work one night, realized that when I do that, all the data is on the phone. If the phone were to be lost or stolen, there would be no way of tracking it using this Tasker Profile. By tweeting to a locked twitter account, I can log in and see where the phone is, remotely, while still keeping the data private.
* Select **Phone** from the 'Select Action Category' menu and then **Send SMS** from the 'Select Phone Action.' In the 'Number' field enter "40404". This is Twitters number for mobile tweets. I will go into more depth in a future post about integrating Twitter and your mobile device. In the 'Message' field enter "GPS Loc: `%LOC`, GPS Acc: `%LOCACC` ft, GPS Age: `%GPS_AGE` min". See photo.
<figure>
  <img src="{{ site.url }}/images/SendSMSdefine-1024x567.png" >
  <figcaption>Define the send SMS function.</figcaption>
</figure>
* And finally, select **Phone** from the 'Select Action Category' menu and then**Send SMS** from the 'Select Phone Action' again. In the 'Number' field enter "40404", in the 'Message' field enter "Wifi Loc: _%LOCN_, Wifi Loc Acc: _%LOCNACC_ ft, Wifi fix Age: _%NET_AGE_ min".

### Using the Profile

I've had the profile running for a few days now and it appears to be working really well! As the image to the right shows, both the location from the GPS and wifi signals (for an explanation of how a location can be determined see this [Google Mobile Blog post](http://googlemobile.blogspot.com/2008/10/my-location-now-with-wi-fi.html)) are reported. The GPS accuracy typically bounces between 96 and 68 ft; the wifi accuracy is typically around 100ft. The GPS fix age ranges from 30 second to 15 minutes and the wifi location fix age is typically less than 30 seconds old. The wifi location fix age, obviously, is much older when the phone is not picking up a wifi signal. Note, though, that the phone does not need to be connected to the wifi signal and transmitting data to use it to determine location. The phone only needs to pick up and identify the wifi signal, i.e. location can be "pulled" from a locked wifi signal.Battery drain appears to be minimal. The Tasker profile was running for a 20 hour period and the battery was only down to about 15% when the phone was plugged into the charger. This is typically of my battery life.

I'll report further as I tweak/fix the system.

<figure>
  <img src="{{ site.url }}/images/sampletweets.png" >
  <figcaption>Sample tweets.</figcaption>
</figure>
