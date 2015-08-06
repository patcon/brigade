# The Code for America Brigade Website

Code for America Brigades are local volunteer groups that bring together community members to help make government work better. Brigades use technology to build new tools to help with local civic issues. Code for America supports Brigade chapters with resources, tools, and access to the wider civic technology movement.

This repo is for the Brigade website [https://www.codeforamerica.org/brigade](https://www.codeforamerica.org/brigade)

## Goals
This website is meant to:
* Get you to sign up for your local Brigade
* Explain what the Brigade program is
* Show off the fine works of the Brigades
* Provide tools that help Brigade work

## History

The Brigade program started in 2012 as an experiment, largely copying the success of [Open Gov Hack Night](http://opengovhacknight.org/). 

This website is on its third version. V1 Was a Rails site with many contributors. It served the Brigade well as it was growing. As Code for America became better at supporting the volunteer groups, we needed something different.

The [CfAPI](http://github.com/codeforamerica/cfapi) was built as reaction to how Brigades were operating themselves. We now meet them where they are, instead of trying to get them to log into our site.

V2 was powered by the CfAPI and worked great, yet was built quickly with PHP and Javascript. It was kind of a cobweb of dependent parts.

V3, the current site, is meant to simplify the code and make it easier for Brigade members to get involved in building the Brigade site.

## Attendance & Check In

Attendance is one of the basic metrics that needs to be tracked in movement building. Its useful for tracking the impact of your outreach, the growth of your group over time, and individual participation tracking. Its also incredibly useful for fundraising, considering many grants will accept volunteer hours as their matching funding requirement.

We've built a platform for your Brigade to start tracking attendance.

* https://www.codeforamerica.org/brigade/attendance
* https://www.codeforamerica.org/brigade/Code-for-San-Francisco/attendance

Brigade members can checkin at:

* https://www.codeforamerica.org/brigade/checkin
* https://www.codeforamerica.org/brigade/Code-for-San-Francisco/checkin

We recommend making a short link of the checkin url for your group.

* https://www.codeforamerica.org/brigade/Code-for-San-Francisco/checkin?event=Hack+Night

#### Build your own Brigade attendance tools

Attendance data can be pulled from the Code for America API.

* https://www.codeforamerica.org/api/attendance
* https://www.codeforamerica.org/api/organizations/attendance
* http://www.codeforamerica.org/api/organizations/Code-for-San-Francisco/attendance

Checkins can be posted

* https://www.codeforamerica.org/brigade/checkin
* https://www.codeforamerica.org/brigade/Code-for-San-Francisco/checkin

The schema expected for checkins is:
```
fieldname - type - default - optional - example
name - string - None - Yes - `Margaret Hamilton`
email - string - None - Yes - `apollo@nasa.gov`
event - string - None - Yes - `Moon Landing`
date - datetime - datetime.now() - Yes - `1969-07-20`
cfapi_url - string - None - No - `https://www.codeforamerica.org/api/organizations/Code-for-Houston`
question - string - None - Yes - "What did you do today?"
answer - string - None - Yes - "I invented software engineering and sent the first people to the moon."
```

## Installation

The Code for America Brigade site is built on [Flask](http://flask.pocoo.org/) and Python with a little bit of Javascript. The `app.py` file describes the routes. The `templates` have the html.

1. Set up a [Python virtual environment](https://github.com/codeforamerica/howto/blob/master/Python-Virtualenv.md).
2. Install the [required libraries](https://github.com/codeforamerica/howto/blob/master/Python-Virtualenv.md#install-packages).

To run locally, ensure that the environment variable `BRIGADE_SIGNUP_SECRET`
is present:

    python app.py

Contacts
--------

* Andrew Hyder ([ondrae](https://github.com/ondrae))

Copyright
---------

Copyright (c) 2015 Code for America.
