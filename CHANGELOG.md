## CMDBuild 3.4 (released 2022-01-28)

### NEW FEATURES:

* Removed legacy shark code
* Removed legacy schemas support: quartz, bim, shark schemas will NOT receive any special treatment any more
* Update jasperreports lib to 6.17.0
* Require java 17+
* Update maximum version of postgres to 12 and minimun to 10
* Deprecation of beanshell: use groovy as default in more places (eval ws, etc)
* Implemented chat notifications and user chat framework
* Add new modular platform waterWAY to manage data
* Manage CMDBuild Service BUS and job logs
* Add Biginteger attribute
* Add multi selection lookup attribute
* Add link attribute
* Handle geoattributes permissions
* Add new property in administration for mapping on documental
* Manage load file DWG directly from the map
* Add the possibility to organize map layers in a menu
* Allow configuration of Info Message on Geo Attributes
* Allow card creation from map
* Add support for markdown on field text
* Add password attribute
* Add formula attribute
* Add file attribute
* Add icon to navigate on field reference to associated card if have permissions on this
* Add domains 1:1
* Manage Groovy scripts
* Add group configuration to manage bulk_update, bulk_delete and bulk_abort for all classes
* Show labels on map elements (all o just a few)
* Add column user's description in history grid
* Allow custom menu configuration for views from join
* Allow inline widgets
* Add button to print the map on pdf
* Added reference relations, other relations and system history in history tab
* Allow geoattributes multi-selection on map
* Asynchronous generation of reports
* Add new BIM viewer Xeokit
* Allow navigation tree as default page 
* Added attachments preview in emails
* Add possibility to set layout for closed processes
* Add possibility to exclude attributes from filter creation
* Added function filter for filters created from the administration module
* Added per-join configuration to enable user privileges filter
* Show widgets on attachment creation

### IMPROVEMENTS:
* Add help field in view when new propriety helpAlwaysVisible is true
* Improved field features editors in administrator module
* Add number of grid records in linkCard widget
* Add hierarchical view in class and process permission management
* Open popup to load file when click on drag area in attachments widget
* Disable forgotten password if allow change password is disabled in administration
* Add save button grid preferences in scheduler page
* Hide SSO authentication buttons if the session exists
* Avoid show simple classes in schedule rule definition class list
* Add order legend grid thematism
* Improve email address validation
* Enable double click on long press popup in map
* Hide button save grid preferences when user is on map
* Add the status of the scheduler service in task list
* Allow negative delay period in schedule rules definition
* Show class name also in extended data relations
* Allow custom filters in UI filters management
* Open all card actions as detail window on map
* Add properties HideInCreation e HideInEdit in widgets configuration
* Improve tabs in BIMsurfer Viewer
* Select all geoattributes creates on the map for a card
* Reorganize menu in administration module
* Add loading mask on calendar widget
* Added error directly on add attachments if it has the same name as the present attachments
* Show always labels input parameter and value on filter
* Add binding in view rules
* Remove localization flag in context menu and form widgets in administration
* Improved speed on menu creation
* Restrict file list based on import template filetype
* Add visual indicating on download loading report

### BUGFIX:
* Fixed form validation on classes
* Add dashboard in administration from section model statistics now work
* In custom menu now is possible to set name elements with spaces
* Ifc import no longer fails on empty attribute values
* Add specific error in bulk edit when no attribute is selected
* Resize window editor script edit now works
* Corrected various translations
* Fixed break map cards list
* Expand card in grid list when select card on navigation tree gis
* Fixed visibility custom pages on custom routing from admin module
* Languages configuration on administration work now correctly
* Expand scheduler record also after refresh
* Group permission header checkbox (select all) if no longer slow if current column is sorted
* Remove geo attributes panel from process in administration
* Correct infinite loop on login page caused by default language not mandatory in administration
* Card deletion after incompatible filter deletion now doesn't cause infinite loading
* Disable sorting column Type in scheduler grid
* Navigation tree loads the correct page when moving through the tree while a card creation panel is open
* Field "Attribute message" in administration for process now filter data
* The query filter on grid is now applied also when the search field is fulfilled
* User default Group is don't clear after selection change on group list
* Correct visibility deletion option fields domains in administration
* Remove support of html and markdown on text attribute of domains
* At login module pressing enter multiple times to perform login now don't break UI
* Dynamic images now working also in subreports
* Fixed error when editing form widgets and window height is small
* Remove notification filter not valid on attribute filter attachments card
* Correct appearance of customForm attributes
* Save button now work correctly in administration for attribute creation
* Clicking on grant column header for processes select all elements
* Now is possible to change direction of recursive domains in menu navtrees
* Active column for lookup values in grid is now sortable
* Add validation input on lookup type and dms category type name
* Email sign placeholder is visible on fullscreen editor mode
* Disable add button also if user has read only permissions in one category in attachments
* Cancel button now work correctly in administration GIS Navigation
* Tree in administration GIS Navigation don't break if change origin class
* Fixed strange behaviour when deleting context menus on classes
* Correct values of ecql filter in linkCard widget
* Correct selection type attribute on administration attribute creation
* Fixed import/export error on retrieve class attributes
* Keep selected elements when updating an advanced filter with a condition on relations
* Grid reload now deselects all elements
* Don't show process without XPDL
* Add possibility to use timeout in file download
* Process notes are now saved even at creation
* Disable possibility to remove attributes from list on import/export domain template
* Task send email don't break UI
* Fixed error on save filters from relation caused by cards attributes
* Enabled classes on domain are empty if "enabled classes" tab is selected before navigation
* Fixed problems on disable classes on domains that weren't working properly
* Link on change module (admin/management) user menu now working
* Select first menu voice on login if default page group isn't set
* Order rules in user menu by traduction
* Remove invalid filter message on filter on column
* At login set the preferred language as the language to use
* Fixed error on calendar rule definition button on date attribute
* Fixed missing configuration content analysis in job read email
* Fixed elimination value on button delete on default page in administration section group and permissions
* Correct fieldset style in views
* Correct ordering columns on relation tab with extended data enabled
* Relation inline are no longer visible in create pop up
* Correct dashboard visualization in administration
* Fixed problem on safari that when the session was expired weren't show login but was empty
* Fixed problem on firefox that custom permissions don't appear the first time you open a grant configuration
* Add tooltip on administrations tool that didn't have it
* Remove infinite loading mask on BIMsurfer Viewer when BIM Project don't have load file IFC
* Add confirm message to delete draft message when refresh grid in manageEmail
* Fixed error when creating a view from filter with filter on relation attribute
* Attribute maxLength is disabled on inherited attribute instead of hidden
* Add class help when create a new card
* Correct position relation graph node description at open popup
* Fixed error when create new process from layouts tab
* Attachment filter is in read only mode on administration if form mode is view
* Add ignore tenant when have set a single tenant
* Fixed error that ignore rows grant on view join not shared
* Show active toggle tool in join view
* Update process form status in administraton if xpdl upload fail
* Fixed error in views from filter that not filtering on attribute used to create view
* Add control in clone card with relations where exist destination domain
* Add pgsql mode to ace editor
* Fixed problem on scheduler that doesn't handle negative delays correctly
* Email templates now show correctly the value of the delay field if equal 0
* Enable search attachment text
* Set etl gates search empty text less generic
* Fixed error in view inline relations that set scrollbar in grid always on top
* Starting url now work if link is to administration
* Fixed error that break interface in administration in tab Disable Classes on domains
* Show key import also when is composed by more than two attributes
* Show correctly delete icon on Safari in schedules attachments
* Fixed clone valor Value on clone import/export template
* Hide view on class if this class is disable
* Fixed loading of nested reports on CMDBuild
* Disable classes not selectable in add card button in relations popup
* Fixed problem on template import for timestamp
* Fixed handling of time attributes in xlsx export
* Manage others HTML symbols in report
* Uploading a lot of documents no longer causes CMDBuild to loses metadata
* Add possibility to filter data on field class in multitenant configuration
* Fixed validations error on import template in administration
* Add possibility to disable editing cell on grid in widget customform
* Add possibility to order columns inside grids when creating relations
* Remove edit button in system on server management administration
* Fixed problem that save the edit mail already present also you click on cancel
* Fixed problem on cron expression on card visualization
* Delete notify popup without message after creating an email account
* Fixed click on translation button on lookupValue from viewInRow in administration

## CMDBuild 3.3.3 (released 2021-12-23)

### BUGFIX:

* Fixed wrong behavior of join view filter with permission
* Fixed issue affecting attachments when querying card from superclass
* Uploading a lot of documents no longer causes cmdbuild to freeze
* Filter request tracking payload (strip sensible auth data)
* Decoded report name in routing to prevent problems with reports which have spaces in name
* Create/modify widget works properly again
* Attributes on domains work again inside inline relations
* Fixed view join permission handling
* Fixed decimal/double printing in card report
* Added context menu handling for superclasses
* Dropped cache after localizations import
* Added basic management for row grant on user join view
* Fieldsets toggle again on Safari
* Added decimal digits as admin definition for double in card print
* Fixed serialization of widgets in card details with no permission
* Fixed translation preload to include file translations
* Infinite loading mask when creating a BIM project with a deleted name no longer happens
* Fixed null serialization of idcardcqlselector in rest v2
* Timestamps in relations are now parsed
* Fixed relation filtering in geovalues
* Fixed issue that prevented processing cad element set with no entity
* Fixed error on customform widget refresh button
* Fixed reference processing for email for cross tenant references
* Deleted bimobjects related to bimproject when removing a project
* State attribute in administration no longer shows system lookups
* Redirected to activity with same subset in process execution
* Value 7 on Day of the week can now be used
* LinkCards widget now opens details on popup
* LinkCards widget now shows inline attachments
* Fixed issue with SMTP configuration with ssl
* Email attachments are now saved before the process advance
* Dropped user class cache after adding/changing xpdl in a process
* Handled attribute permission in card serialization rest v2
* Handled rotation of dwg elements in dwg import
* Avoided serialization of dms categories in class structure when disabled
* Deleting process layout now sets record to null
* After changing password the page now returns to precedent page correctly
* Patched gis tables to set IdClass default value
* Added possibility of sorting for card relations
* Shown user messages when file download fails
* Fixed attachments serialization with null category when dms category is disabled
* Add attachments from the document archive doesn't break the UI anymore
* Added support for multiline strings
* Added filtering based on _type for card relations
* Disable widget if class is undefined
* Fixed rest v2 dms category id serialization
* Handle comma in email reference header
* Reloaded menu item after card creation on nav tree root
* Manage Attachments on closed activity now works if active in the configuration system and disable on the process
* Double click on attachments row now opens the attachment if user hasn't write permissions on that category
* Added custom fieldsets in custom dms models
* Fixed issue when processing reference values within cql expressions
* Custom pages on custom routing are now visible from admin module
* Fixed error on attachments preview if name contains []
* Import domain tamplate validation no longer fails
* Updated language cookie before user preferences save
* Fixed issue when processing inactive processes with invalid wf provider
* Added check on custom components loading to get js files only in management module
* Always renew activity instance id after activity is completed
* Ui no longer crashes on compulsive domain change
* Added translations description for Category and FileName fields
* Included widgets and contextmenus in class/process translation tab
* Detailed view is now serialized on view update
* Refreshed grid view in row on active toggle click
* Added missing padding in Notes tab
* Domains tab is no longer enabled on simple classes
* Email signatures can now be deleted
* Multi-selection is again deselectable
* Opening last grid card after deleting last card loads again inline on Firefox
* Navigation trees no longer shows disabled domains on administration
* Fixed update of only one custom component
* Fixed behavior of search user in All Users list
* FormWidget now handles correctly cql variables and expressions
* Edit card button is now enabled for inline relations inside "Create / Modify Card"
* Removed error template from import export template configuration
* Fixed geoserver layer upload errors
* Added active attribute to gis geoserver layer
* CreateModifyCard no longer throws error if reference is not set
* Restored missing geo style rules params
* Attachment counter now handles dms permissions
* Fixed grants sorting list by mode
* Fixed sorter handling when attachment filter is applied
* Firefox no longer generates error on saving attribute twice
* Fixed gis and relation navtree circular domains
* Removed disabled classes from domains
* In custom components and custom page, files fieldset are now visble in view mode
* Enable/Disable button for dashboard now works as expected
* Fixed issue when processing cad import context filter
* Error downloading report in CSV format has been solved
* Incoherent behaviour when deactivating GIS layers visibility has been fixed
* Changed csv encoding default value
* Disabled reports are now shown in admin module
* Fixed minor cad import issues
* UM position values are now translated
* Promoted caches to system to avoid hourly refresh
* Added session refresh when active requests on session cleanup
* Cql for masterdetail domains is no longer ignored
* Ok button in admin view on filter now works as expected
* Calendar widget values no longer disappear
* N:N domain now supports inverse relation
* Database import are now shown in task manager
* Clone dwg template from detail window is now supported
* Fixed generic Errors on Groups and permissions
* Fixed attachment category permission handling
* Removed detailed=true when making events request
* Fixed error shown when advancing process when in superclass
* Domain name is visible again when editing reference attribute
* added support for external dumps with env folder
* Fixed issue in join view query when processing out of order table join
* Gis navigation now manages view mode
* Polygon geometry are now shown on GIS map
* Added composite filter validation
* Enabled contextual menu button items on maps
* Roles are now shown translated
* Added auto cleanup of attachments missing on dms
* Removed load mask affter the loading of the first page
* Added auto cleanup of attachments missing on dms
* Default template for data import config no longer makes the template unselectable
* Administration lookup search is now working as expected
* Changing session timeout no longer breaks the interface
* Descriptions of objects under administration are no longer considered valid if they contain only spaces
* Import management combo no longer crashes the ui
* Fixed generic error when deleting class
* Fixed start new workflow with soap updateWorkflow function
* Added support for different APM in soap attribute list serialization
* Added language header in rest preload function
* Sanitized notes/metadata of card attachments
* Join view loader is no longer stuck after save if attribute grouping contain spaces
* Fixed bug in menu folder translation saving
* Added fulltext attachment search support for SharePoint dms
* When typing in view with filter atrtibute dropdown in administration fields no longer get reset
* Fixed permission handling for relation graph
* Set multitenant mode on processes is now working as expected
* Fixed regexp used to display tousands separator
* Expand view record is no longer slow
* Dasbhoard pop-up is now working properly
* Menu is now ordered correctly again
* User activation botton is working again as expected
* Restored missing foreignkey triggers
* Fixed issue with relative location gis import, when reference points to superclass
* Disabled cad hatch parsing

## CMDBuild 3.3.2 (released 2021-05-04)

### NEW FEATURES:

* Added search possibility on the categories and on the metadata associated with the documents attached to the data cards
* Possibility to set permissions on attached documents different from those of the class they belong to
* Added download all button for cards attachments
* Added email signatures
* Added possibility of exporting process data as well as class data
* Added possibility of filtering processes based on the current step
* Possibility of saving in the user preferences the sorting of the columns in the grids
* Enabled the use of contextual menu in the map view
* Added column filters on Simple classes
* When adding content from navigation menu the relation will be created by the system and the menu will refresh
* Added plugin management of the different SSO authentication available (CAS AD/LDAP, SAML 2.0, ADFS 4, OAUTH2 KEYCLOAK, etc.)
* Added the possibility for the user to choose one of the enabled authentication methods at the login
* Added SSO authentication at webservice level
* Added the possibility of consulting in the Administration Module the active authentication methods and the parameters set for each
* Added loading spinner in content header and in form body
* Performance improvements

### BUGFIX:

* Grid view in row on active toggle click now correctly refreshes
* Fixed multitenant message in administration module
* Domains tab enabled on simple classes is no longer enabled in administration module
* Improved email expr processing to use client/server card data
* Multi-selection is now again deselectable
* Opening last grid card after deleting last card now correctly loads inline on Firefox
* View with join now allows attribute named 'description'
* Fixed bug that prevented the update of max length for string attributes
* Navigation trees no longer shows disabled domains in administration
* Mananged tenant change when user has not enabled multi-tenancy
* Fixed bug that prevented search user in "All Users" list
* Tab details is no longer always enabled
* FormWidget now handles correctly cql variables and expressions
* Removed desktop custom pages in mobile menu serialization when using Default
* Edit card button is now enabled for inline relations inside "Create / Modify Card"
* In admin navigation trees skip node creation if source or destination class is disabled
* Removed error template from import export template configuration because never used
* Parameters for component context menus are now correctly handled
* Fixed geoserver layer upload issue
* Fixed processe instances ordering by tenant id
* Fixed error that prevented handling of domain attributes in join view
* Import/export database password field is now hidden
* Data export now fails if template contains disaled attributes
* Fixed internal cache refreshing mechanism to avoid periodic cache drops
* Fixed various navigation tree wrong behaviors
* Fixed Import/Export template clone errors
* Fixed error that prevented CQL for master/detail domains from being used
* Fixed bug that prevented ok button in admin view from working
* Calendar widget values no longer disappear
* Added widgetId where missing in widget data
* Database import templates are now shown in the task manager
* Files whose name contains [ ] no longer give bad request on download request
* Fixed error that prevented translation of geo-attribute from administration
* Fixed error that prevented Domain name to be shown when editing reference attribute
* Default Import/Export combos are now updated after add or remove template
* Fixed system config decimal separator validation
* Gis navigation now manages view mode
* Grant filter icon is no longer higlighted if column privileges are default
* Polygon geometries are now shown on GIS map
* Roles are now shown translated
* Fixed decimal comparison when checking changed attributes in import
* Default template for data import no longer makes the template unselectable
* Fixed error that prevented lookup search from working properly
* Changing session timeout no longer breaks the interface
* Object under administration are no longer considered valid if they contain only spaces
* Fixed lookup value in schema print to show translated description
* Fixed filter support for geoAttributes get center function
* Fixed start new workflow with soap updateWorkflow method
* Join view loader no longer gets stuck after save if attribute grouping contains space
* Fixed Bug in menu folder that prevented translation saving
* When typing in view with filter attribute dropdown in administration fields no longer reset
* Fixed cross site scripting related issues
* Added permission for relation graph
* Fixed error that prevented setting multitenant mode for processes
* Fixed total count in view with join card list
* Fixed issue that prevented open import/export template from class
* Fixed domain description translation in card report
* Dasbhoard pop-up now works properly
* Menu is now ordered correctly
* Restored missing foreignkey triggers
* Print csv grid no longer uses thousand separator for numeric fields
* Fixed Join view when handling domains with the same code of a class
* Fixed administration issue for import gis template validation
* Fixed issue with relative location gis import, when reference points to superclass
* Node creation if source or destination class is disabled is now skipped
* createModifyCard no longer throws error if reference is not set
* Avoided serialization errors in widget rest v2
* Fixed error that prevented geovalues from being loaded in particular cases
* Restored missing geo style rules parameters
* Fixed order by Tenant field in grids
* Fixed error that was generated on Firefox when saving attribute twice
* Removed disabled classes from domains
* Enable/Disable button for dashboard does no longer generate errors
* Menu nav tree active toggle button no longer generates error
* Calendare event description/content are now correctly translated
* Fixed regexp unexpected identifier on Edge and Firefox
* Improved administration history dashboard
* Fixed error that prevented downloading report in CSV format
* Fixed incoherent behaviour when deactivating GIS layers visibility
* Fixed add card in filter view
* Fixed default map zoom issues
* Relation is no longer created when card created from master detail with no reference field
* Disabled reports are now shown in admin module
* Fixed various cad import issues
* Admin module: UM position values are now translated

## CMDBuild 3.3.1 (released 2021-01-26)

### NEW FEATURES:

* Views with joins
* CSV import with multiple keys
* Attachment fulltext filter
* Dynamic images inside reports
* Contextual help for process steps
* Added support for new filter operators for lookup and references
* New operator "from filter" in relations filter
* Allow attachments and email widgets at first step of a process
* Included IFC data in BIM View
* Dasboard improvements: open charts in popup and chart download as image
* Added configuration to use a custom page as default view for classes or processes management
* Added Mongolian localization

### BUGFIX:

* Fixed multiple bugs related to dashboard in administration module
* Fixed attachment extension check to avoid extension case
* Fixed dashboard wrong order in output parameters bug
* Fixed getCardHistory soap function
* Changing dms model of a dms category no longer breaks the UI
* Fixed erroneous administration module grants preview bug
* Fixed check if filter with same name already exist in save filter
* Fixed configuring read email task bug that caused UI to not load
* Fixed tasklist serialization with usage of user permission
* Fixed ordering inconsistency by automatic sorting by Id if available
* Disabled selection for not available records in add and edit relations
* Fixed superclass ordering by subtype, used translated subtype description
* GIS selected item are now transparent
* Fixed filter on attribute name from bulk edit
* Added loadmask when loading localization
* Creating a new process in administration now refreshes the side menu
* Fixed attribute group translation inheritance
* Domain filter cql is no longer deleted on domain update
* Groupings of attributes is now be visible on create
* Applying schedules on DMS class no longer breaks UI
* Fixed issue in impersonate api/processing
* Dropping existing layout on process forces a page refresh
* Removed relations serialization of non active domains
* Fixed error that prevented scheduler rule to not be shown correctly
* Fixed error that prevented cloning IFC import template
* Fixed duplicated records in menu navigation trees
* Fixed nav tree direction processing in gis value service
* Filtered away geoattributes in classes without permission
* Fixed issue with default resizer for text area on Firefox
* Adding new attribute on Layout tab no longer removes all items
* Fixed issue for batch job run
* Fixed empty html in IE on report refresh
* Fixed date reading format bug
* Fixed issue in navigation tree when multiple domains on the same level
* Improved execution time of bimserver project upload
* Removed inactive class filters from filter list endpoint in management
* Fixed bug that prevented the removal of uncategorized attachments
* Fixed record not expanded correctly on inline attachments related bug
* Fixed issue in email image processing
* Normalized Associated Card field name in new BIM project
* Fixed email read job configuration regex parameter bug
* Selecting Report from menu when process is expanded no longer causes errors
* Fixed relations inline bug on map
* Fixed issue in embedded item loading
* Fixed bug on multitenant page
* Updated Batik libs from 1.7 to 1.8
* Fixed passive mode configuration parsing
* When group doesn't have a default page UI doesn't show a blank page anymore
* Fixed email processing for uncommon inline content disposition
* Fixed issues in stats query
* Fixed bug that prevented "Import Key attribute" to not be shown on Explorer
* Popup no longer closes at first scheduler event creation in management
* Card ws PUT Request now returns ref/lookup code and desc when no changes are made
* Widget LinkCards now updates the rows after edit when a trigger has delays
* Improvements in Import IFC
* Handled tab separator in class print as csv
* Fixed attribute group translation for process ws rest v2
* Administration attribute header bar title now uses Code instead of Description
* included _LookupType and value in ddlog whitelist
* Various ifc job configuration fixes
* BIM projects "Last checkin date" is no longer editable


## CMDBuild 3.3 (released 2020-09-16)

### NEW FEATURES:

* Added new administration dashboard
* Added logs administration panel
* Bulk update and delete of cards
* New IFC file connector
* New DWG import templates
* Added nested navigation tree in menus
* Import database and gis task
* Added mobile custom components handling
* Added possibility of handling cascade deletion for domains/relations
* New DMS system handling
* Permission handling for custom components
* Added form help text
* New extended realtion header
* Indonesian localization
* Polish localization


### BUGFIX:

* Fixed missing translation flag in Menu > Navigation tree > Description
* Fix issue that prevented bottom border of the view tab panel from showing
* Allow `a` tags (links) in strict html attr values
* Fixed issue that caused wrong sorting on menu navigation trees items
* History tab is no longer empty if fieldset is closed by default
* Fixed bug that prevented click on map point in superclass view
* Added possibility of updating style of system/protected lookup values
* Set tenantid to default user tenant when create/update with null tenantId
* UI no longer crashes after de-selecting "include Inherited" in admin module
* Fixed issue that prevented button "Send Email" from administration module to be used
* Translation panel now handles Activity and Group type
* Opening the filter of a view no longer crashes the UI
* Attachment file type check is now case insensitive
* Fixed issue with target device filtering
* Updated custom components constraint to include TargetType
* Deleting card without relations now consider relations with U/N status
* Added load mask in attribute creation
* Added notification tab in Database, GIS and IFC tasks
* Relation graph no longer crashes UI
* Order of relations shown in management module now reflects the order set in the admin module
* Fixed issue in user preferences processing
* Fixed issue related to format date on filters
* Import/Export template now also uses tab separator
* Fixed server processing of ecql with LookUps
* Added statistics for task Import IFC in administration home
* Prevented error if class or process is disabled
* Added step activity translations in translation panel
* Added Groups translation section server side
* CQL filter now works on GIS navigation tree
* Fixed cascade delete gis values on card delete
* Added support for float4 (float) column type
* Handle template expressions in cal event description, content
* Allowed users to list bim projects
* Handle relation attributes when updating a card with a reference
* Added configs for system jobs
* Ui no longer breaks when re-opening template after save
* Fixed serialization of calendar triggers with admin viewmode
* Added format config for import/export csv
* Fixed class relations get when without domains
* Fixed issue that prevented clone card to properly work
* Improved english core translations
* Added active/inactive item filter for class calendarTriggers, ctx menu, widget, formTriggers
* Fixed issue in embedded items processing
* Fixed issue that prevented "x" button to delete the default account in the email templates to be shown
* Calendar events don't lose values anymore
* Fixed Error in main routing condition code
* Various rest v2 response improvements/fixes
* Fixed various IE UI issues
* Added X-Mailer and other debug header to email sent from cmdbuid
* System config disable inactive user checkbox is now unchecked by default
* Added filter options in reference selection
* Search filters are now ordered
* Removed preset field from dms config page
* Reordering attributes of a DMSModel no longer throws an exception
* Removed limits in geoattributes request
* Added missing labelField translation in dashboard charts serialization
* Various dashboard related issues have been fixed
* Fixed issue that prevented customwidget tooltips to be hidden
* After deactivating domains grid is now refreshed to show new value
* Added ecqlfilter in charts
* Improved relations attributes management in add relation grid
* Fixed wrong grid date render
* Query relation now works with superclass
* Added handling of multiple application names in same entity for Dxf Reader
* ForeignKey in inline import now has code and description
* Fixed inline import/export param handling
* Attribute grouping no longer causes bug on save
* Fixed issue related to long filter marks
* Geoserver layer ws now accepts both id or code
* Fixed widgets id handling
* Added usage of componentId for custom context menu
* Search field in administration now resets on page change
* Added configuration to disable inactive users
* Session menu now filters custom pages without permission and avoids error
* Removed dms models from role grants endpoint
* Reduced default maxLoginAttempts time window to 60 seconds
* Fixed query for group user list
* Fixed issue related to calendar event notification
* Handled precision and scope attrs for function output of numeric type
* SubclassFilter is no longer ignored if subclassViewMode=cards
* Fixed cache issue when processing geoserver layers
* Sql patch now always sets process provider to shark for proper process migration
* Removed download button, upload xpdl for superclasses
* Added sorter/filter for email endpoint
* Save and apply filter no longer opens popup below filter panel
* Fixed issue with RiverFlowid inconsistency
* UI no longer breaks after click on reference attribute linked to the scheduler
* Prevented save of empty filter
* Fixed administrator layout panel bug when trying to remove column
* Fixed issue related to widget data serialization
* Autovalue is now working properly in "details" tab
* Added geoserver version check
* Textarea fields now expands correctly
* Removed old unique indexes on EmailTemplate and EmailAccount
* Geoserver workspace is now autocreated if not existing
* Refresh button on gis view now reload tiles
* Added drop cache event for domains after class delete
* Added relation information in card print
* Added missing domains in schema report
* Inline notes are now editable when create or modify a card
* Server now returns null when widget produces Lookup/reference with id -1
* Active toggle button no longer causes error on detailWindow
* Task workflow attribute list is no longer editable in VIEW mode
* Text parameter is now handled by dashboards
* Process instances list is no longer called twice
* During process creation the print button is now disabled
* Added attachments and email count for process instance webservice
* Scheduler's days advance are no longer ignored
* Fixed issue affecting permission filter returining null
* Added dms model print schema functionality
* Fixed issue with dms document update on alfresco
* Added full calendar trigger info within detailed attribute response
* Fixed issue when processing (duplicate) noactive references
* Fixed issue in cal event notification preview
* Fixed lookup type validation for dms cat
* Fixed model layout tool buttons permissions related issues
* Expanded process record is no longer blank under certain circumstances
* Added tenant check for import, using default tenant if required
* Removed permission check when executing impersonate from wf script
* Subclasses now inherit calendar triggers for inherited attributes
* Fixed cmis attachment preview related issues
* Deleting lookup value no longer breaks UI
* Fixed report permission check related issues
* Improved menu item description/targetDescription processing
* Added print schema button on processes like classes
* Added calendar event attachment management
* Master detail (MD) CQL filter is now working as expected
* Fixed error on file check in send import report
* Widget linkCard no longer breaks if query result is empty
* Added unique client identifier header for all REST requests
* Inline attachments now show attachments
* Added attributes filter on request to get only Id and Description
* Fixed error on reference editors inside grids
* CustomForm widget reference description is no longer empty
* Preselect if unique works again on LookUps
* Handled _status attribute in process instances filter
* Fixed issue in embedded items processing
* Added cascade info for domains
* Fixed Javscript error handling for schedules condition


## CMDBuild 3.2.1 (released 2020-04-22)

### NEW FEATURES:

* Completion of the control page in the Administration Menu of the various services used by CMDBuild, and possibility of consulting/downloading the log files;
* Completion of the password management, with the possibility of blocking it in the event of repeated failed authentication attempts and not proposing its modification function in the case of centralized authentication;
* GIS improvements, with display of the list of elements around the “clicked” point and with an icon for the direct passage from the GIS Tab card to the corresponding card;
* Possibility to limit, in the Administration Module, the extensions allowed for the attached files;
* Possibility to configure, in the Administration Module, the list of languages ​​proposed at login.


### BUGFIX:

* Added missing fields in process rest v2
* Attribute types for standard and simple classes are not longer wrongly displayed
* Meta field is now always available in rest v2
* Fix error that prevented email to be attached to card after a scheduled event
* Fixed error on creating import/export template with merge criteria
* Translations template email in import csv
* Schedule definition rule grid is now updated after active change from detailWindow
* Added owner description in geolayers response
* StartWorkflow widget is no longer hidden on processes
* LinkCards widget no longer generates error for non-admin users when target class is a process
* When deleting dashboard used by menu in administration UI no longer keeps loading
* Mixed improvements for etl import notification processing
* Fixed send error email notification for import job, when file is missing related issues
* Fixed gis attribute processing related issues
* Fixed multitenant on simple class related issues
* After class delete, added cleanup grant and menu
* Fixed issue in log message processing (session expiration)
* Fixed issue in cluster message processing after rpc add
* Fixed server response of etl template
* Avoided fatal error when a menu item is missing in admin view
* Fixed issue in smart expr processing
* Fixed global script config for xpdl
* Fixed widget data serialization
* Enable/Disable button for geoattributes works again as expected
* Non active geoattributes are again shown in management
* Fixed issue that prevented a new attribute window from closing and refreshing
* Fixed formInRow of importExport record related issue
* Fixed various errors in rest v2 serialization
* fixed report endpoint rest v2
* Superclass grid is no longer hidden when user saves default filter and does not save columns preferences
* Calendar is no longer hidden for write permissions
* UI config are no longer saved inverted on change permissions in "other permissions" tab
* Widget openNote is again working as expected
* Fixed issue related to composite filter attribute mapping
* Added beginDate to geoserver layer serialization
* Fixed context menu label translation issue
* Fixed error when listing completed process instances
* Reorder grids no longer breaks UI
* Multi-level lookup no longer shows only last level in the grid
* Added instance name translation
* Deleting a filter just saved now correctly removes it
* Fixed issue with uploadreport cli command
* Boolean 3 phase checkbox now owrks on mobile
* Non SuperUser users now sees to whom the process is assigned after executing it
* Fixed sorting from superclass based on _type
* Reload button in dashboard graphs now works as expected
* Dashboard in demo database no longer causes error in function output
* Fixed error on opening #administration/domains/
* Grid on openAttachment widget now loads values when opening
* 'Clone from' in administration module now works as expected
* Fixed groovy dependencies
* Basedsp properly wors again for SQL views
* Default language for user is now correctly handled
* startWorkflow widget output variable is no longer always null
* Date column is now correctly displayed
* Import csv for domains without 'merge criteria' now properly works
* Fixed ecql/easytemplate expr processing related issues
* Enabled widgets on card creation
* Changing column privileges no longer alters row privileges
* Fixed Bad JSON in _Form Data section related issues
* Fixed issue that prevented the correct label to displayed while creating a new group
* It is now possible to delete the group if selected
* Fixed ui for new post-csvimport send report (bypass file attachment check)
* On process creation the ui no longer sends not needed GET call for related filters
* Admin ui now handles new config params for attachment file check
* When receiving error after email template deletion UI now refreshes correctly
* Tenant is no longer hidden for some classes
* Client now checks for attachment file types
* Fixed issue in etl processing when import key is a reference
* Widget linkCard is now correctly self-valued if the defaultValue is set
* Grid is now updated after active change from detailWindow
* Required link card now saves data correctly
* Fixed error generating mail for import job when file not found
* Remove geoattribute no longer causes not needed calls to other geoattributes
* Grid of assigned templates no longer hides the templates
* Default class import/export template can again be saved
* Class and Process category lookup no longer show id instead description
* Template for import csv for domains now has IdObj1/Idobj2 attributes
* Fixed "download report" button for InternetExplorer
* Error notifications no longer shows json instead of message
* Fixed issue when processing etl import with null values in key attr
* Fixed access denied for non admin users on context menu call related issues
* DefaultSelection on widget linkCard now works as expected
* Fixed mark processing for superclass query
* Attribute list columns of a class no longer get stuck
* Fixed query reference code/descr processing related issues
* Reference field is no longer hidden if its description is not in card data



## CMDBuild 3.2 (released 2020-02-06)

### NEW FEATURES:

* Management of the Dashboards, recovered from CMDBuild 2, with some improvement features (see next news);
* Management of the Scheduler, fed either automatically by operating on data cards or manually (see the complete description here);
* Extension of user preferences: home page, customization of lists of data cards (choice and width of columns and sorts), default filter for each class;
* Restoration of Wizard Connector tasks, for the visual definition of synchronization templates of external database tables with CMDBuild classes;
* New types of permissions on processes (in the case of using permissions on the lines of a class, possibility to specify the permission to be applied on extra filter lines);
* Checking of password definition criteria;
* New GIS implementations: completion of the thematism, display of objects present around a point on the map, search for an address;
* Display of the status of the various server services used by CMDBuild;
* New role of “limited” administrator with the possibility of creating users on his Tenant;
* Sign On authentication on LDAP systems through the use of the open source CAS service.
* Core security improvements
* Restws and core test additions
* Added Malaysian localization

### BUGFIX:

* Fixed disabled actions for permissions related issues
* Import export tasks now require an email account
* Fixed various url malformed issues
* Import export templates are now shown in the permission tab
* 'Remove filter' button on views now works properly
* Privileged user flag is now properly saved
* Ui configuration in permission tabs works properly again
* Fixed 'initial page' related issues
* Fixed issue that prevented a process to be executed even with all required fields set
* Reference arrays are now handled in custom widgets
* Fixed issues that prevented a reset of searchbars in the administration module
* Fixed import export templates clone related issues
* Restored missing sql functions for openmaint databases that prevented the usage of multitenancy
* Improved card detail panel UI behaviour
* Error messages during login phase are no longer displayed after succesful login
* Fixed UI issue that prevented a card from being open with a double click interaction
* Fixed process menu button interaction when workflow is disabled
* Fixed issue related to automatic email generation
* STARTTLS and SSL can no longer be activated together in email account creation
* Inline relation of N:N domain no longer shows only one direction
* Fixed issues related to superclass query filter processing
* Quicksearch in group permission now gets cleared after group change
* Fixed issues related to Add Group button in administration
* Fixed issues related to double expression processing in email templates
* Fixed issues related to UI interaction with IE 11
* Fixed issue related to date parameters in process widgets
* UI no longer breaks after attribute deletion on class
* Fixed inconsistency with multitenant class mode in administration
* Fixed process permission handling related issues
* Create/modify card widget no longer breaks
* Email account no longer gets removed following an error
* Fixed positionOf related issues
* Deleting the single card of a class no longer leaves the UI in a loading phase
* Fixed issues related to total metadata processing on last page
* Fixed issues related to starting group processing
* Workflow task process attributes are again correctly parsed
* Date attributes are no longer wrongly displayed when client timezone is changed
* Fixed endpoint rest v2 for attachments download
* Fixed validation rule not applied to text attributes with HTML editor
* TextArea for text fields can now be resized correctly
* Fixed issue that caused malformed date attribute in soap response
* AllowCardEditing for linkCard widget properly works again
* Prevented redirect if no url is defined after navigation render
* Fixed email delay processing value to be in seconds, not milliseconds
* Fixed issues related to attribute translation processing
* Process Hide save button works again properly
* UI no longer gets stuck when opening completed processes
* Lookup list with ecql properly returns the correct results again
* Fixed issue that prevented class context menu translate icon to not appear
* Fixed multiple attachments for email related issues
* Delete domain from class or process domain tab properly removes the domain from menu
* Deleting a superclass in administration now properly refresh the class inheritance dropdown
* Fixed issues related to header param CMDBuild-View
* Fixed issue that prevented multitenant mode translation to be shown
* Custom status of processes is no longer lost at every update in admin mode
* Fixed issues related to webapp installation under ROOT folder
* Fixed sql expression escaping when setting session variables
* Fixed issues related to filters on date fields
* Validation rules are no longer wrongly cancelled in search filters
* Basedsp properly works again for SQL views
* Fixed issues related to interaction with master/detail tab
* Fixed issues related to usage of reference parameters in reports
* Fixed issue that prevented import export administration menu voice to be shown
* UI no longer gets stuck when refreshing a grid with one card only
* Fixed issue related to multilevel lookups with three or more levels
* Fixed issues related to card put endpoints for rest v2
* Attribute grouping translation is no longer broken
* Fixed issues related to special characters handling in rest webserices
* User menu no longer displays an empty row
* Invalid search filters can no longer be saved by the ui
* Fixed issue that prevented IP_ADDRESS attribute type to handle IP range
* Data card sorting is no longer missing in processes
* Fixed issue that caused the interface to be stuck in loading after saving a csv report
* Fixed issue that prevented the UI to load when moving from a custom page to a process page
* Fixed issue that prevented time attributes to be displayed correctly in the history page
* Fixed issue that prevented emails to be processed with utf encoded file name
* Fixed issue that prevented email attachments to be processed when with same filename
* Fixed session login date default value
* Fixed timezone processing issue
* Fixed date/timestamp attribute issue for domains
* Edit button for class domains properly opens the correct panel again
* Fixed custom widget data processing for rest v2
* Fixed email processing after import job is completed
* Fixed ddl log regexp related issues
* UI now allows scrolling through filter list
* Relations tab with no relations no longer generates errors
* Attachment category description is again properly translated
* Validation rules are again working for lookup values
* LinkCard widget no longer opens a blank popup
* Removing default groups no longer freezes the UI
* Fixed issues related to wrong serialization of report attributes in rest v2
* Fixed issue that prevented filters to be removed from group and permission tab
* Fixed issue that caused the login page to display disabled groups
* Fixed issue that caused the UI to not refresh after adding a new user
* Fixed attribute search in class panel
* Fixed issue that caused the UI to freeze after multiple clicks
* Fixed email template pagination



## CMDBuild 3.1.1 (released 2019-09-25)

### NEW FEATURES:

* Added administration interface to create a personalized layout for the data cards of each class
* Cookie handling has been moved server side to improve the security of the application
* Added handling of Boolean null values
* Improved UI for handling processes with parallel activities
* Added form triggers on processes for the execution of personalized behaviours
* Added Bulgarian localization

### BUGFIX:

* FlowStatusAttr send the description instead of Code
* Fixed Id tenant related issues
* Column filter now handles null booleans
* Added validation on reference attributes
* Fixed process abort related issues
* Added active field for search filters
* Denied creation of reference on non active domains
* Improved check before class deletion
* Fixed bim related issues
* Avioded errors when invoking sessions/current to check an existing session
* Fixed reports related issues
* Fixed process save button related issues
* Updated redirects when a page is not found
* Fixed datefield on Firefox browsers related issues
* Added custom widget components interface
* Fixed attachment mandatory description related issues
* Fixed search filter scrollbar related issues
* Fixed attribute grouping related issues
* Fixed page refresh related issues
* Avoided cache loading loop when processing grants on filters
* Fixed clone card and relations related issues
* Fixed 'Active' checknox of class domains related issues
* Fixed domain localization window related issues
* Added row count in user grid
* Fixed permissions for attribute 'Notes' related issues
* Added popup size properties in system configuration
* Added massive relation modification web service
* Fixed print csv from superclass related issue
* Improved execution time of domain list
* Added exception when email storing fails
* Fixed attribute group modification on Firefox browser related issues
* Fixed dms description attachment related issues
* Added optional task list informations in process instances webservice
* Fixed error popup in applypatches screen
* Normalized request id
* Fixed checkbox not appearing in card view
* Added options to improve flow migration performance
* Added parameter to set to null values on migration error
* Avoided description deletion for uploadcustompagedir rest command
* Forced save of only edited grants
* Handled single/multi group in Process Activities
* Added client api to open report
* Added Save and close button in processes edit form
* Fixed missing scroll on relation attributes
* Add condition in view model to prevent null parent errors
* Lookup codes can now start with a number
* Fixed class translation related errors
* Added segments field to geostylerules
* Mail queue scrollbar is now visible
* Allowed custom colors on lookups
* Fixed GeoServer layers loading related issues
* Reload flow status after task completion
* Added stored filter description translation in filter webservice
* Managed double click on inline domains
* Handled `@MY_GROUP` and `@MY_USER` in attribute filter values
* Impersonate with group only is now allowed
* Fixed csv domain import related issues
* Handled objects names containing spaces
* Search filters now shows the mandatory input marker
* The grid after proces closure is now refreshed
* Code, description data for client card when processing email template are now loaded
* Fixed widget related issues
* Menu now loads when all resources are loaded
* Form structure for classes are now correctly stored
* Implemented attachments.download() function
* Handled menu migration with faulty `null` childs
* Fixed date attribute in soap response
* Custom pages now handle active field
* Fixed password autocomplete=off
* Fixed null performer related issue
* Fixed report lookup parameter reset issue
* CQL filters now work inside reports
* Fixed open related card issue
* Added attachment api support
* Email queue administration page now refreshes when email are sent
* Fixed deletion of Import/Export template
* Reports no longer break when parameters have spaces
* Lookup values are now loaded on model generation
* Default class order in now used in csv export
* Fixed incorrect date format in xls export issue
* Fixed changed detection on history related issues
* Added task description translation
* Added task widget description translation
* Handled "Add attachments to closed activities" permission as global parameter and group-level privilege
* View search now affects grid elements
* Improved beanshell script error processing
* Improve handling of csv line number
* Handled status/FlowStatus attribute in card print webservice
* Fixed workflow permission filter on webservice `processes/x/instances`
* HideSaveButton system default is now used when retrieving single process hideSaveButton informations
* Removed binding on process add button
* Handled preselectIfUnique in rest webservice parameters
* Fixed and improved lookup handling in soap webservices
* Fixed cron expression interface related issues
* 'State attribute' value on Processes tab no longer changes from edit to view mode
* Fixed erroneous handling of metadata total field
* Views ParameterType runtime are now properly working
* Filters are now displayed correctly
* Added scrollbar on card's notes
* Handled pagination for views webservices
* Allowed duplicate participant definition while processing xpdl participants
* Unified custom component management on database
* Improved relation permission handling


## CMDBuild 3.1.0 (released 2019-07-10)

### NEW FEATURES:

* Csv/xls[x] import/export (manual or scheduled)
* Configurable sso integration module ( _services/custom-login_ )
* Improved security, support for _PBKDF2_ password protection
* Improved workflow upgrade
* Improved cli utils
* Added gis tematic mapping
* Restws and core test additions
* Possibility of displaying the attached files as an additional fieldset of the data card
* Possibility of displaying the relationships of a domain as an additional fielset of the data card
* Extension of the “Show if” feature as “View rules”
* New feature "Auto value" for fields
* Synchronization between the filter applied to the list of data cards of a class and the corresponding elements displayed on the map
* New custom components that can be used in context menus
* Possibility of uploading the customer's logo which is placed alongside the CMDBuild one
* Added Danish localization
* Added Norwegian localization

### BUGFIX:

* Recovery of the process startup task in the Task Manager
* Report are now translated in menu
* Added uploadcustompagedir command to upload a custom page via rest command
* Reserved domain relations are no longer being shown
* Added configuration to hide save button in workflow
* Added user sorting
* Added card ws distinct option
* Added system config to set relation limit
* Added detail parameter to menu ws
* Geo attribute deletion is no longer generating errors
* Added new feature to center a map when no items are selected
* Added print view function
* Removed unused sorters
* Removed screen flashes in login form
* Added ws to obtain a boundary box for attribute values
* Multiple filter/roles no longer generates a server error
* Added basic fulltext filter for geo style rules
* Added auto redirect to url on login if redirect config is not empty
* Forced usage of subclass instead of superclass model to create cards in reference combo popup
* Attachment widget various fixes
* Added possibility of resize of textareas in attributes administration
* SimpleClass.BeginDate is now reserved
* Processing of int values in numeric xls columns is no longer broken
* Various minor fixes for BIM administration
* Fixed skipunknowncolumns template processing related issues
* Apache poi has been upgraded
* PresetFromCard has been implemented
* Fixed LockNotAcquired error
* Button to remove filters in administration module is no longer broken
* Fixed filter processing related issues
* Gis icon preview now automatically refreshes when updated
* Minor fixes for Icon management
* Group and permission default filters are now saved
* Email widget serialization for rest v2 is no longer broken
* Allow more then one row expanded in history grid
* Default filter on Class are now saved
* Stop queue button is now disabled when queue is not enabled
* Ip type attributes are no longer forced to IPV4
* Multilevel and cql filter have been removed from bim layers
* Gisnavigationtree and bimnavigationtree now have active toggle button
* Added endpoint to obtain class domains
* Added geostyle rules put endpoint
* Fixed query builder related issues
* Changed filter format in rest v2 class attribute response
* Fixed errors in process instances rest v2
* Added configurable strong password algorythm
* Fixed permission of subclasses
* Litteral `{` is now supported in email template
* Fixed widget serialization for rest v2
* Added tenant column hidden in grids
* Fixed relation attributes related issues
* Fixed start activity related issues
* Uniformed tenant label to other labels
* Added geo style rules application without saving on db
* Fixed occasional errors on add form mode in permission page
* Lookup attributes in card relation ws are now handled
* Upload report is no longer broken
* Fixed rest v2 process instances response
* Class -> Domains -> Form are no longer missing 'View' tool button
* Fixed domain errors on new form
* Fixed advanced filter related bugs
* Added system configuration for default email account
* The form of navigation tree is now in view mode after edit
* Domain grids now hide 'M/D, Label M/D, Inline' columns
* Doubleclick on geoattribute grid no longer breaks ui
* Gis icon upload now refreshes the grid
* Input fields no longer make Firefox crash
* Added ws to query distinct values from a class
* LinkCards output is no longer null
* Auto skip email with no TO address (set directly to status `skipped`)
* It is now possible to create/edit workflow widgets in classes edit form
* Domain button from process tab is no longer broken
* Date filter no longer looses the date values
* Process history is no longer missing data
* Load activity in process instance is now specified
* Option to create a default menu is no longer missing
* Fixed calendar related issues
* Process instance history is no longer missing data
* Detail window in administration module is no longer staying open when changing context
* Fixed between filter related issues
* Menu list in administration module no longer shows Code instead of description
* Fixed icon related errors in administration module
* Improved class/process save/upload
* Reports no longer remain stuck in loading
* Nav tree with multiple nodes for the same class are now handled
* Multiple selection flags are now correctly updated
* Wf is now allowed to start with no-db performer
* Added full request log tracking
* Fixed csv stream processing related issues
* Fixed advanced filters with boolean attributes
* Removed popup error after logout
* Reduced system configuration changes processing time
* Combo for class/process/... now shows original description
* Sort option on permission page is no longer broken
* Reserved classes are no longer shown in grant ws
* Card filter for geo value query are now handled
* Localization page now ignores processes if workflow is not active
* Fixed class and process icon related issues
* Fixed geo attribute and gis icons related issues
* Menu shows again source folders in edit/add
* Tooltip no longer overlaps with custom validator
* Added support for function filter
* Now map reads initial configuration ZoomMaz, ZoomMin, InitialZoom, Longitudine, latitudine
* Mousewheel has been disabled on numeric fields
* Fixed hidden relations related issues
* Existing locales of class attribute description are no longer blank
* Process advancement no longer remains in loading
* Migration script now handles unique indexes
* Fixed class creation related issues
* Added system configuration endpoint
* Improved performance of attribute reorder
* Added missing SOAP functions
* Added cli tool to check dump
* Fixed master/detail tab simple class related issues
* Fixed fkdomain ws filter
* Added `isMasterDetail` filtrable attribute
* Added print schema
* Added, on db restore, option to freeze (not expire) existing sessions
* Added backup config files before update
* Attribute filters in report parameters are now handled
* Cmis selection is now forced in DMS settings
* Grid over window size in now scrollable
* Added card print for cards with `"` in attribute label
* Added new wd migration (from shark via db)
* Permission flags in relations are now handled
* Added view card print
* Added wf api for update/advance process
* Card access (tenant) is now checked for relation update/delete permissions
* Default for groups in filters is now saved
* Foreign keys are no longer shown as integer
* Fixed domain active field related issues
* Menus in administration navigation are now sorted
* Added geoserver file handling
* Added uptime to restws cli status report
* Added lookups migration with description for code
* Card display is no longer stuck on loading
* Select all in link card is now possible
* Added email template ws v2
* Fixed typeAhead related issues
* Added attachment category description translation
* Processes description is now translated
* Added client api to get remote lookup from type and code
* Added withCard() method to wf email api
* Added download zip CustomPages
* Modified date serialization on custom form widget
* Menu with already open popups now correctly closes
* Implemented newMail wf api method
* Removed unnecessary store filters
* Fixed custom form widget related issues
* Added missing file/dir error in job import
* Wf card api now returns boolean values
* Added default for showInGrid and writable properties in custom form widget
* Added user config for preferred office suite
* Added defaultSearchFilter in Reference popup instead of variable in viewmodel
* Added process stoppableByUser field in response
* Fixes various issues related to header auth
* Added navigation rule for views in menu after render event
* Implemented findAttributeFor for local wf api
* Fixed parallel gate wf processing related issues
* Clear model attributes in CustomForm widget panel
* Added edit possibility of card from linkCards widget
* Prevent special characters in dynamic model fields
* Added configuration to send always all fields to the server in PUT requests for cards and instances
* Fixed eval sql query related issues
* Functions with non-lowecase names are now handled
* Added add attachments to card via cmdb api
* Added case insensitive processing of `TYPE: function` comment value
* Fixed custom page component processing related issues
* Cleanup of user friendly messages for common import errors
* Fixed order grid details problems
* Fixed import of ipvAny attribute related issues
* Fixed editing relations related errors
* Added properties on grant model
* Email.delay param is now handled in seconds and not milliseconds
* Cm filter keys are now case-insensitive
* Req id is now included in popup messages
* Domain functions minor refactoring
* Added configuration parameter for column offset in import template
* Fixed ws v2 description translation related issues
* Default class filter are now correctly saved
* Added timezone in user config preferences
* Grant eventbus refactoring
* Added custompages active filed
* Card attribute reference fields now accept empty strings
* Fixed support for startsWith and endsWith in strings for IE11
* Added creation of fictitious menu


## CMDBuild 3.0.0 (released 2019-04-12)

### NEW FEATURES:
* Complete rewriting of the user interface, both for the Data Management and the Administration Module, with new layout and new functionalities.
* Complete refactoring of the server code.


## Previous versions

For the CHANGELOG versions up to 2.5.1 view http://www.cmdbuild.org/en/download/changelog-old
