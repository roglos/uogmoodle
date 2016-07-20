UOGMOODLE
=========
We wont actually store Moodle in this folder as it can be retrieved from the moodle github account directly.

It is planned not to  make any changes to core moodle code at any stage.
Therefore this repository is set up to make use of the Wiki and Issues pages to document installation and development
of Moodle at university of Gloucestershire rather than the core code.

For instructions for cloning moodle code see below - more detail on:
https://docs.moodle.org/31/en/Git_for_Administrators

INITIAL CLONE OF MOODLE
=======================
cd /path/to/your/webroot
git clone https://github.com/moodle/moodle.git  //Use the https version to prevent port blocking
cd moodle
git branch -a
git branch --track MOODLE_31_STABLE origin/MOODLE_31_STABLE
git checkout MOODLE_31_STABLE

INITIAL CLONE OF OTHER PLUGINS
==============================
Several of these plugins do not exist as github repos
They have been created as such for internal management
of code and development.

** All plugins MUST be added to the .git/info/exclude folder to minimise issues when upgrading **
** All directories are given based on being in the parent moodle directory unless stated **

XAPI LOGSTORE
cd admin/tool/log/store
git clone https://github.com/xAPI-vle/moodle-logstore_xapi.git xapi
cd path/to/moodle

TURNITIN - INSTALL AS A GROUP OF INTERDEPENDENT PLUGINS
cd blocks
git clone https://github.com/turnitin/moodle-block_turnitin.git turnitin
cd ../mod
git clone https://github.com/turnitin/moodle-mod_turnitintooltwo.git turnitintooltwo
cd ../plagiarism
git clone https://github.com/turnitin/moodle-plagiarism_turnitin.git turnitin
cd path/to/moodle

COURSE FORMATS
GRID
cd course/format
git clone https://github.com/gjb2048/moodle-format_grid.git grid
cd path/to/moodle

HELIX - MEDIAL
cd lib/editor/atto/plugins
git clone https://github.com/roglos/moodle-atto_helixatto.git helixatto
cd ../../tinymce/plugins
git clone https://github.com/roglos/moodle-tinymce_helixmedia.git helixmedia
cd ../../../../mod
git clone https://github.com/roglos/moodle-mod_helixmedia.git helixmedia
cd assign/submission
git clone https://github.com/roglos/moodle-assignsubmission_helixassign.git helixassign
cd path/to/moodle

LIBRARY RESOURCES
cd blocks
git clone https://github.com/roglos/moodle-block_library_resources.git library_resources
cd path/to/moodle

RICHARD'S ADDITIONAL RECOMMENDED PLUGINS
========================================
cd theme
git clone https://github.com/bmbrands/theme_bootstrap.git bootstrap
git clone https://github.com/roelmann/moodle-theme_flexibase.git flexibase
git clone https://github.com/kennibc/moodle-theme_pioneer.git pioneer
git clone https://github.com/gjb2048/moodle-theme_essential.git essential
git clone https://github.com/moodlerooms/moodle-theme_snap.git snap
cd course/format
git clone https://github.com/gjb2048/moodle-format_topcoll.git topcoll
cd ../local
git clone https://github.com/moodlehq/moodle-local_codechecker.git codechecker
cd ../report
git clone https://github.com/mikasmart/benchmark.git benchmark
git clone https://github.com/moodleou/moodle-report_customsql.git customsql
cd ../blocks
git clone https://github.com/deraadt/Moodle-block_progress.git progress
git clone https://github.com/deraadt/moodle-block_completion_progress.git completion_progress
git clone https://github.com/jleyva/moodle-block_configurablereports.git configurablereports
git clone https://github.com/lsuits/block_quickmail.git quickmail
git clone https://github.com/marxjohnson/moodle-block_quickfindlist.git quickfindlist
git clone https://github.com/marxjohnson/moodle-block_quickcourselist.git quickcourselist
git clone https://github.com/roelmann/moodle-block_course_contacts.git course_contacts



FULL INITIAL SETUP BSH SCRIPT
=============================
cd /path/to/your/webroot
git clone https://github.com/moodle/moodle.git uniglos
cd uniglos
git branch -a
git branch --track MOODLE_31_STABLE origin/MOODLE_31_STABLE
git checkout MOODLE_31_STABLE

git clone https://github.com/xAPI-vle/moodle-logstore_xapi.git admin/tool/log/store/xapi

git clone https://github.com/turnitin/moodle-block_turnitin.git blocks/turnitin
git clone https://github.com/turnitin/moodle-mod_turnitintooltwo.git mod/turnitintooltwo
git clone https://github.com/turnitin/moodle-plagiarism_turnitin.git plagiarism/turnitin

git clone https://github.com/gjb2048/moodle-format_grid.git course/format/grid

git clone https://github.com/roglos/moodle-atto_helixatto.git lib/editor/atto/plugins/helixatto
git clone https://github.com/roglos/moodle-tinymce_helixmedia.git lib/editor/tinymce/plugins/helixmedia
git clone https://github.com/roglos/moodle-mod_helixmedia.git mod/helixmedia
git clone https://github.com/roglos/moodle-assignsubmission_helixassign.git mod/assign/submission/helixassign

git clone https://github.com/roglos/moodle-block_library_resources.git blocks/library_resources

git clone https://github.com/bmbrands/theme_bootstrap.git theme/bootstrap
git clone https://github.com/roelmann/moodle-theme_flexibase.git theme/flexibase
git clone https://github.com/kennibc/moodle-theme_pioneer.git theme/pioneer
git clone https://github.com/gjb2048/moodle-theme_essential.git theme/essential
git clone https://github.com/gjb2048/moodle-format_topcoll.git course/format/topcoll
git clone https://github.com/moodlehq/moodle-local_codechecker.git local/codechecker
git clone https://github.com/mikasmart/benchmark.git local/benchmark
git clone https://github.com/moodleou/moodle-report_customsql.git report/customsql
git clone https://github.com/deraadt/Moodle-block_progress.git blocks/progress
git clone https://github.com/deraadt/moodle-block_completion_progress.git blocks/completion_progress
git clone https://github.com/jleyva/moodle-block_configurablereports.git blocks/configurablereports
git clone https://github.com/lsuits/block_quickmail.git blocks/quickmail
git clone https://github.com/marxjohnson/moodle-block_quickfindlist.git blocks/quickfindlist
git clone https://github.com/marxjohnson/moodle-block_quickcourselist.git blocks/quickcourselist
git clone https://github.com/roelmann/moodle-block_course_contacts.git blocks/course_contacts

