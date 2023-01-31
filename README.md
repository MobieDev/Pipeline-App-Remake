# Pipeline-App-Remake
Remaking a past full-stack Node.js application of mine into a Google Workspace web application.
The README documentation for the original project is below. The remade app will include all the same functionality as the original app, along with an updated interface design.

# ---------- 

# Pigging Operations History and Schedule
Thinkful fullstack capstone project, a Pipeline Pigging Operations History and Schedule app which allows pigging activities to be historized and scheduled.

## Introduction

The Pigging Report is an Excel workbook which contains several different types of data: the pigging histories of the pipelines, the pigging schedule, the operators' daily field reports, and the pipeline debris trending reports. It also contains information about each pipeline, such as pipe size, valve types, and acceptable pigs. 


This application replaces the current Pigging Report, helping teams be more effficient by saving time managing their report. This application will also stabilize the data by reducing the number of times it is handled and by standardizing data input.


## User Stories

This application will be utilized by four different types of users: Pipeline Operators,  Pipeline Foremen, Production Foremen, and Managers.

* As a User, I want to login so that I can use the application.

* As a User, I want to reset my password if I have forgotten it so that I can log in to the application.

* As a User, I want to create an account so that I can use the application.

* As a User, I want to view and update my account information so that I can change my password.

* As a Pipeline Operator, I want to input my daily pigging activities so that I can track my work on the pipelines.

* As a Pipeline Operator, I want to record pigging exceptions (times when a pig was not launched on schedule) so that the launch schedule will remain up-to-date.

* As a Pipeline Operator, I want to record notes about my location observations so that other operators can be aware of hazards.

* As a Pipeline Operator, I want to view the pigging schedule so that I can plan my field route.

* As a Pipeline Operator, I want to view the previous launch details so that I can understand why pigs are overdue.

* As a Pipeline Foreman, I want to view daily pigging schedules so that I can prioritize the tasks of the operators.

* As a Pipeline Foreman, I want to view the details of the previous launch so the I can understand why pigs are overdue.

* As a Pipeline Foreman, I want to view the debris reports so that I can adjust the pigging frequencies if necessary.

* As a Pipeline Foreman, I want to trend pigging activity so that I can track costs and plan spending.

* As a Pipeline Foreman, I want to view pigging history so that I can identify missing launch and receive data.

* As a Pipeline Foreman, I want to be able to update the pigging history so that I can correct mistakes.

* As a Pipeline Foreman, I want to add pipelines to the application so that I can add them to the pigging schedule.

* As a Pipeline Foreman, I want to update pipelines information so that I can correct mistakes and keep the data current.

* As a Pipeline Foreman, I want to remove inactive pipelines from the pigging schedule so that I do not mistakenly send an operator to pig an inactive pipeline.

* As a Pipeline Foreman, I want to assign user roles so that I can control access to the pigging data.

* As a Pipeline Foreman, I want to deactivate users so that I can control access to the pigging data.

* As a Pipeline Foreman, I want to change user roles so that I can control access to the pigging data.

* As a Production Foreman, I want to view the pigging schedule so that I can plan field operations around the scheduled pigging activities.

* As a Manager, I want to view the debris reports so that I can remain informed about my department.

## Business items (database structure)

* user
    * role (Pipeline Operators,  Pipeline Foremen, Production Foremen, and Managers)
    * email (email)
    * password (password)
    * first name (string)
    * last name (string)
    * active (boolean) (default value = true)

* report centers
    * name (string)
    * number (integer)

* systems
    * name (string)

* pipeline
    * report center name (string)
    * report center number (integer)
    * name of the system (string)
    * name of the pipeline (string)
    * launcher site name (string)
    * receiver site name (string)
    * size of pipeline (string)
    * type of product (string)
    * type/name of acceptable pigs (string)
    * closure information (string)
    * pigging frequency (string)
    * date added, updated, or removed (timestamp)
    * active (boolean)

* pigs
    * types/name (string)
    * size (string)

* pigging activities
    * pipeline name (string)
    * exception (string)
    * asigned user email (email)
    * notes (string)
    * launch timestamp (timestamp)
    * receive timestamp (timestamp)
    * launcher site name (string)
    * receiver site name (string)
    * debris found at the receiver site (string)

* debris collected from the pipeline
    * pipeline name (string)
    * receiver site name (string)
    * type (string)
    * weight in pounds (integer)



## Functionality

The app's functionality includes the following abilities:

- login with a username and password
- view daily pigging schedule
- enter and submit daily pigging activities
- make notes about launch and receive exceptions
- view pipeline pigging history
- add new pipelines to the history and to the schedule
- add new users
- remove users
- modify and correct the pigging history
- create debris reports which trend type and amount of debris collected within specific timeframes

## Wireframes
![Wireframe _User Login](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_login.png)

![Wireframe _Reset Password](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_reset_password.png)

![Wireframe _Create Account](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_create_account.png)

![Wireframe _Account Info](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_account_info.png)

![Wireframe _Operator Input Pigging](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_input_pigging.png)

![Wireframe _Operator Pigging Schedule](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_operator_pigging_schedule.png)

![Wireframe _Operator Previous Launch ](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_operator_prev_launch.png)

![Wireframe _Foreman Admin Menu](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_admin_menu.png)

![Wireframe _Foreman Pigging Schedule](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_pigging_schedule.png)

![Wireframe _Foreman Previous Launch](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_prev_launch.png)

![Wireframe _Foreman Debris Reports](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_debris_reports.png)

![Wireframe _Foreman Pigging Activity](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_pigging_activity.png)

![Wireframe _Foreman Pigging History](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_pigging_history.png)

![Wireframe _Foreman Update History](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_update_history.png)

![Wireframe _Foreman Add Pipeline](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_add_pipeline.png)

![Wireframe _Foreman Update Pipeline](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_update_pipeline.png)

![Wireframe _Foreman Add User](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_add_user.png)

![Wireframe _Foreman Update User](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_foreman_update_user.png)

![Wireframe _View Only Pigging Schedule](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_viewonly_pigging_schedule.png)

![Wireframe _View Only Debris Reports](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/wireframes/wireframes_viewonly_debris_reports.png)


## Notes

The priorities of the design of this application were:
1. use by the Pipeline Operators
2. use by the Pipeline Foreman
3. use by Users logging in
4. use by New Users ceating accounts
5. use by the Report Viewers

The Pipeline Operators and Foremen will access the application utilizing an iPhone 6 or later using Chrome or Safari as the web browsers.



## Screenshots

![Screenshot _Login Page](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/login-page.jpg)

![Screenshot _Create Account Page](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/create-acct-page.jpg)

![Screenshot _Update User Access Page](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/update-user-access-page.jpg)

![Screenshot _Admin Menu Page](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/admin-menu-page.jpg)

![Screenshot _Input Pigging Page](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/input-pigging-page.jpg)

![Screenshot _Add Pipeline Page](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/add-pipeline-page.jpg)

![Screenshot _Pigging Schedule Page](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/pigging-schedule-page.jpg)

![Screenshot _Previous Launch Page](https://github.com/KSherrell/pipeline-pigging-ops-fullstack-capstone-project/blob/master/public/imgs/prev-launch-page.jpg)


## Future Fixes

* Admin pages "Pigging Activity", and "View Pigging History" will be created.


## Tech Notes

This application was created using

* HTML5
* CSS
* jQuery
* Javascript
* Node.js
* Express
* MongoDB
* Mongoose
* Heroku
* Linux Ubuntu / Oracle VM VirtualBox
* Windows 10
* Brackets
* Robo 3T


