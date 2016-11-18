# Change Log
All notable changes to pre-ignition will be documented in this file.
Pre-ignition adheres to [Semantic Versioning](http://semver.org/).

We are using [this tool](https://coderwall.com/p/5cv5lg/generate-your-changelogs-with-git-log) to generate part of automated changelog.

## [0.8.0]
Unreleased 
### Added 
- [ ] buttons that induce server interaction show when waiting for server answer (e.g. check email or verify terms)
- [ ] [use a map instead of combo for geographic selection ](https://gitlab.com/christophe-g/pre-ignition/issues/12)
- [ ] Assign businesses to steward managers (drag and drop tool)
- [ ] Implement Glossary in questions
- [ ] First version of terms of service
- [ ] Animated new logo
- [ ] Online-Offline indicator
- [ ] Include proper transition when lazy loading
- [ ] Add validity for counting a question as completed (e.g. comment are valid only if length > 10)
- [ ] Live edit of surveys sections (for testing surveys section by section)
- [ ] Add connection detector (only display when offline)

### Modified
- [ ] upgrade url routing (new version of app-route)
- [ ] upgrade to new version of Firebase API (v.3) so as to enable uploading of documents.
- [ ] Present the survey as a self-assessment test - propose to share findings with potential investors
- [ ] Remove currency information from `appCurrent`. Instead add one additional parameter like `localeCurrent`
- [ ] More advanced editing for questions (domainRange, ...)
- [ ] Augment metadata for filled-in questionnaire (business id in particular)
- [ ] Review Navigation (follow best practices from app-route in (shop app)[https://github.com/Polymer/shop]). 
- [ ] Decide on better workflow dataModel (workflow belongs to program Coverage - what is the relationship between workflow and questionnaire )

### Fixed
- [ ] Survey navigation button killing url routing sync. (url route and view were not in sync anymore)
- [ ] Problems with question values not being set under android tablet
- [ ] Lookup from firebase not working properly (e.g. default workplan). First need to upgrade to Firebase SDK 3.0
- [ ] The error message on logout is cryptic


## [0.7.1]
Unreleased
Focus: whatever was not ready for [0.7.0]

### Added
- [ ] One page for ABB Bangladesh
- [ ] Agri-specific section

### Modified
- [ ] Finalize review of scoring values
- [ ] Format number for Money ...

### Fixed
- [ ] Update language dialog appear the second time we log-in 
- [ ] Sometimes, completion information is reset
- [ ] Disconnect firebase-document on error

## [0.7.0]
Released: 2016-11-19
Focus: prepare for production app

### Added 
- [x] Coverage manager - user with rights to administer/follow-up accounts and data associated to a specific program coverage (e.g. ABB Bangladesh)
- [x] Portfolio management page (incl. BCM, notes on the company)
- [x] Event for coverage (e.g. new connection, new busineses, ...)
- [x] See who is online for a specific coverage
- [x] Improve login experience : update view when we are actually trying to login
- [ ] Image url in user profile
- [ ] Guidance for options (e.g. type of business registered)
- [ ] Visualize all comments under admin
- [ ] Basic help wiki for coverage
- [x] Online presence tool (e.g. track user presence, session, online and offline status)
- [x] show user status in coverage (online/offline/idle)
- [x] Store coverage information (e.g. ABB_BGD) on client the first time they enter the app
- [x] Integrate program coverage into questionnaire preliminary checks and workflow (e.g. ask 'where are you using preigition if this info is missing')
- [x] View Survey comments under user profile
- [x] Load data on analytics (not automatically)
- [x] Tool to remove user and user data
- [x] Migrate and test data to new production domain 
- [x] Have a way to show that we are using the test database
- [x] New Gitlab repository with public access for release notes and bug reporting.  

### Modified
- [x] New business profile page
- [x] Checks prior to the survey are now a separate web-component (survey-check)
- [x] Changed the way we register membership (user belonging to admin or dev group)
- [x] Improve/simplify main homepage
- [x] Improve accessor for lookup items (new web-component lookup-accessor that build an accessor funciton) 
- [x] Review dropdown-menu binding with database 
- [x] Finalize screening questions 
- [x] Improve the way feedback are stored in the dB (and security/index rules)
- [x] Better way to indicate missing fields 
- [x] Integrate Questionnaire review / feedback
- [x] Attach scoring to Business and not the questionnaire itself

### Fixed
- [x] Problem with finance section not marked as completed
- [x] Debt-option not working well
- [x] New section are not being stored in the db (need to consolidate mech for checking initial data)
- [x] Cursor focus and scroll after profile verification completion
- [x] Navigation menu is inactive sometimes at startup 
- [x] click on menu with href link sometimes does not activate the relevant link (when clicking on borders)
- [x] Business verification process not updated in the workflow indicator
- [x] Team section does not complete event when all questions are answered
- [x] Investment section look weird
- [x] Questionnaire Navigation (with paper-fab) activates sections that are disables (e.g. social impact or environmental impact)
- [x] Sort on table with accessor function is not working (paper-datatable)
- [x] favicon not linking to the correct one
- [x] Problem when login : need to click twice
- [x] Survey Feedback not saved
- [x] x-scroll is active on main home page 
- [x] Wrong number of input in feedback
- [x] Redirection after login not always working
- [x] Firebase permission error after create account
- [x] manifest.json not served on test.preignition.org (problem with SSL cert.)

### Commit details 
[see here](https://github.com/preignition/public/blob/master/releaseNotes/v0_7_0.md)

## [0.6.3]
Released: 2016-11-02
### Added 
- [x] Program coverage in admin/settings
- [x] Coverage stewardship
- [x] Possibility to identify program coverage from the url (e.g preignition.org/main?coverage=ABB_BGD)
- [x] Preliminary work for portfolio management 
- [x] Improved ways of handling business <-> coverage <-> programm <-> coverage Steward relationship
- [x] New section for Environmental impact

### Cheched
- [x] use domain for redirecting surveys. Status: (Firebase does not support sub-domain for multi-tenant application yet)[https://groups.google.com/forum/#!searchin/firebase-talk/subdomain$20tenant%7Csort:relevance/firebase-talk/UpKNSDsICgc/9hCXbXe8BQAJ]

## [0.6.2]
Released: 2016-10-29
### Added 
- [x] Added possibility to have a printer-friendly version of the questionnaire

### Fixed
- [x] Database lookup on collection added multiple times  

## [0.6.1]
Released: 2016-10-19
### Added 
- [x] Clicking on a business row in analytics now opens the scorecard

### Fixed
- [x] required fields passed as required="false" are now recognized as falsy.

## [0.6.0]
Released: 2016-10-18
Focus: analytics
### Added 
- [x] First go at analytics as screening SME tools
- [x] new multivariate analysis library (multi-verse)
- [x] new multivariate analysis library (multi-chart)

## [0.5.2] 
Released: 2016-09-30

### Fixed
- [x] View weight not working anymore
- [x] Edit question from survey not working anymore (we now only have a rapid edit tool from the survey itself, the rest of the survey edit is done via the admin panel)
- [x] Redirect after create group is not correct

## [0.5.1] 
Released: 2016-09-16 

### Fixed
- [x] Maximum call stack error when going from `HOME` -> `ADMIN` -> `HOME`

## [0.5.0] 
Released: 2016-09-16 

Focus: workflow, admin panel (user membership, survey building tool), various bug fix.

### Added 
- [x] First version of survey workflow (workflow building tool, attaching workflow to survey and workflow indicator when user fills-in the survey)
- [x] First version of surveys building tools (surveys, section and questions. Drag and drop features for constructing surveys and sections structure)
- [x] Versioning of sections and surveys through survey build (e.g. snapshot of a survey at a given time. This enable tracking changes in the questions or section composition)
- [x] Better way to handle translation of questionnaires and translated resources.
- [x] Standardize storing of resources and locale (database object containing translated versions of text).
- [x] Ability to filter list of survey items (surveys, sections, ...)
- [x] Add Program object. Programs are a way to group users under different preignition schemes (e.g. ICCO ABB, VSO, ...)
- [x] Users membership management for admin users (app access right driven by user memberships, e.g. only access to questionnaire, or able to see analytics)
- [x] Ensure that non authenticated users cannot access protected pages.
- [x] Add default 404 page on application page (admin and main app).
 
### Modified
- [x] [better client-side data verification mechanism](https://gitlab.com/christophe-g/pre-ignition/issues/13) 
- [x] [de-normalize survey questions](https://gitlab.com/christophe-g/pre-ignition/issues/53). Questions belong to a large question pool and survey section link to this pool.
- [x] Better handling of locale data (all data that might exist in more like one language like survey label)
- [x] Better management of url rooting 

### Fixed
- [x] dropping an item (in workflow) creates an error
- [x] scorecard text no appearing
- [x] unable to select items from survey menu

### Commit details 
[see here](https://github.com/preignition/public/blob/master/releaseNotes/v0_5_0.md)

## [0.4.3]
Released: 2016-08-07 

### Added 
- [x] fallback route when no url can match
- [x] Handle 2 different version of d3.js (dc.js - used for analytics is not compatible with the latest version yet!)

### Fixed
- [x] Youtube thumbnail are now fetched over https
- [x] App freeze when user change language
- [x] Navigation from login to main app not working (lazy load on main-app.html not triggered)
- [x] Loading overlay not disappearing when loading app from login page
- [x] User cannot create a new account

### Commit details 
[see here](https://github.com/preignition/public/blob/master/releaseNotes/v0_4_3.md)


## [0.4.2]
Released: 2016-08-02 

### Modified
- [x] More compact build (gaining 50% of file size)

## [0.4.1] 
Released: 2016-08-01

### Added 
- [x] Theme switcher : allow the user to choose its theme for the application
- [x] User info when the application is not the same version as last session
- [x] Page for "more info", "connect with investors" 
- [x] Implementation of [service workers](https://www.polymer-project.org/1.0/toolbox/service-worker) for better experience in offline and spotty network situation.

### Modified
- [x] Core refactoring (massive) so as to be able to be better prepared for HTTP2 and use polymer CLI [detail of the changes](http://gitlab.com/christophe-g/pre-ignition/commit/9edc48aa8e2a157e7d199d38edefeb93f472f968)
- [x] Homepage infographics improved (hovering effect, step number in the title)
- [x] Cleaner use of url for routing (use full url instead of hash )

### Commit details 
[see here](https://github.com/preignition/public/blob/master/releaseNotes/v0_4_1.md)

## [0.4.0]
Released: 2016-07-27
Focus on questionnaire.

### Added
- [x] Homepage infographic on how it works
- [x] [Refine scoring mech](https://gitlab.com/christophe-g/pre-ignition/issues/56): Some questions might lead to 2 scores (e.g. net profit for which we might have %increase score and absolute value score)
- [x] Implement domainFactor for calculating score where we the domain depend on user-data (e.g. a score that depend on the reporting currency )
- [x] New type of scoring scales (e.g. log scale) for non-linear value questions (e.g. profit where a difference between 2000 and 5000 is more important than 200000 and 230000). 
- [x] [weight mechanism](https://gitlab.com/christophe-g/pre-ignition/issues/57): change maximum score for a section if certain criteria are not filled-in (red-flag questions)
- [x] View live scoring for testing the tool 
- [x] Progress bar at the top reflecting percentage completion of section
- [x] Build matrix layout
- [x] New way to edit questions directly on the questionnaire (click + Shift key)
- [x] Improve edit question features (scale, domain, rangeFactor, tooltip and scaleType)
- [x] Reporting currency in profile (readonly value once set). Numeric entries use this currency to display the unit of measure.
- [x] [screening question for some section (e.g social impact)](https://gitlab.com/christophe-g/pre-ignition/issues/61)
- [x] [screening question at the beginning of the questionnaire (only display appropriate survey when some criteria are fulfilled)
- [x] Video page, with filters according to video tags. Video metadata saved on the database, with youtube id as firebase key
- [x] Thumbnail on video (#58)
- [x] Options for direct feedback on question. 
- [x] Separate the survey app from analytics
- [x] [Scorecard : customized text for each section according to actual score](https://gitlab.com/christophe-g/pre-ignition/issues/25)
- [x] New webComponnet for question container (it will handle hte business logic for calculating score, validation and section completeness)
- [x] New webComponnet for for sliders (augment paper-slider so as to have the same behavior as paper-input )
- [x] [Add a new matrix component - implementing data-binding](https://customelements.io/PolymerEl/paper-input-matrix)

### Modified 
- [x] Homepage
- [x] More elegant (and more flexible) way to check section completed and calculate score - we loop through the dom and not through survey model.
- [x] Tooltip on question instead as on question options. Tooltip active only when hovering over (i) icon (#59)
- [x] [feedback more visible](https://gitlab.com/christophe-g/pre-ignition/issues/60) (directly on the section, rather than as a button on the questionnaire) 
- [x] [Styling problem in the survey, e.g. matrix radio button is not styled properly](https://gitlab.com/christophe-g/pre-ignition/issues/55)
- [x] Re-organize certain fields as matrix (e.g. turnover over years ...)
- [x] We no longer load all survey data at once (causing performance issues), but only section data - when it is needed 
- [x] survey data are no longer stored under their surveyId (e.g. pre-ignition). Now they all go to the same global bucket.
- [x] Revised version of questionnaire implemented
- [x] Ripple effect on Menu
- [x] Ripple effect on Video
- [x] Use button instead of link for password recovery
- [x] Screen width threshold for collapsing drawer menu (now 992px)
- [x] Integrate new version of d3 (v.4) and create optimized bundle.

### Fixed
- [x] Radio button not picking the correct key for setting value
- [x] Total number of questions not always properly calculated
- [x] Governement skills options are in the right format
- [x] Question within questions not accessing their config values 
- [x] Firebase query against country and district fired too early (path not fully set)
- [x] Error message toast not closing 
- [x] Some option keys not found when setting data 
- [x] Minified menu not setting tabs
- [x] Width of drawer menu inconsistent in fixed mode (jumping width)
- [x] components not having focus and creating an error
     
### Commit details 
[see here](https://github.com/preignition/public/blob/master/releaseNotes/v0_4_0.md)

## [0.3.1] - 2016-06-27
### Modified
- [x] New user are logged-in once a new account has been created
- [x] e-mail saved on profile when user logs-in with email/psw

### Fixed
- [x] language preference problems are solved (late bind with profile)
- [x] Firebase error when trying to load data too early is corrected (en-bn language lookup)
- [x] User profiles are created when a new account is created
- [x] workflow before fill in the questionnaire bug (not working for new users, profile not being created)
- [x] new user have problems fill-in the questionnaire just after their first login (trying to access the survey causing maximum call size stack exceeded)
- [x] Business location dropdown not properly instantiated

### Commit details
[see here](https://github.com/preignition/public/blob/master/releaseNotes/v0_3_1.md)

## [0.3.0] 
Released: 2016-06-23

### Added 
- Improved workflow before being able to start the questionnaire (need to be logged-in, need to check email address, need to agree on terms of services)
- Load performance improved (mainly due to the change on video wrapper, preventing youtube PAI to be loaded for all videos)
- improved weighting for question answers relative to others (e.g. percentage increase)
- personalized scorecard
- Video wrapper 
- Business profile
- Small logo app for voting
- Language management
- Possibility to edit questions directly from the app

### Changed
- Questionnaire definition is now in the database
- Use of test.preignition.org domain
- Server version of Firebase (now using Firebase 3.0 - upgrade client side not yet implemented)
- Homepage improvement
- New theme with modern colors
- Logo 
- Split of data between survey data and business data

### Fixed 
- Scrollbar freeze
- Questions are in the correct order
- Firebase OAuth problems (not being able to login on the preignition domain)


## [0.2.0]
Released: 2016-06-12
First working version of the app

### Added
- First version of questionnaire
- Login/logout with email/password and gmail account
- Simple homepage
- Scoring algorithm
- Score card
- Questionnaire feedback
- Video added to the questionnaire
- Main template for the app based on <app-layout/>
- Routing based on <carbon-route/>
- Profile Page
- Modified colors for a more modern theme


## [0.1.0] 
Released: 2016-02-11
Pre-ignition Prototype

### Added
- Basic analytics based on dummy data, 
- Basic questionnaire

# Comments 
- we are using `chlogm =  !sh -c 'git log $1...$2  --pretty=format:\"- %s [view commit](http://gitlab.com/christophe-g/pre-ignition/commit/%H) \" --grep="#log"' --reverse` to generate the detailed changelog.