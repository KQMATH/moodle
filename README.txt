This repo exists to make one patch, in the feat/lti-block-hack branch.

*Purpose*: Show block plugins in activities used over LTI.
*Patch* 
--- a/enrol/lti/classes/tool_provider.php
+++ b/enrol/lti/classes/tool_provider.php
@@ -311,9 +311,12 @@ class tool_provider extends ToolProvider {
             exit();
         }
 
-        // Force page layout to embedded if necessary.
+
+        // Force page layout to secure if necessary.
+        // // Force page layout to embedded if necessary.
         if ($isforceembed) {
-            $SESSION->forcepagelayout = 'embedded';
+            // $SESSION->forcepagelayout = 'embedded';
+            $SESSION->forcepagelayout = 'secure';
         } else {
             // May still be set from previous session, so unset it.
             unset($SESSION->forcepagelayout);


                                 .-..-.
   _____                         | || |
  /____/-.---_  .---.  .---.  .-.| || | .---.
  | |  _   _  |/  _  \/  _  \/  _  || |/  __ \
  * | | | | | || |_| || |_| || |_| || || |___/
    |_| |_| |_|\_____/\_____/\_____||_|\_____)

Moodle - the world's open source learning platform

Moodle <https://moodle.org> is a learning platform designed to provide
educators, administrators and learners with a single robust, secure and
integrated system to create personalised learning environments.

You can download Moodle <https://download.moodle.org> and run it on your own
web server, ask one of our Moodle Partners <https://moodle.com/partners/> to
assist you, or have a MoodleCloud site <https://moodle.com/cloud/> set up for
you.

Moodle is widely used around the world by universities, schools, companies and
all manner of organisations and individuals.

Moodle is provided freely as open source software, under the GNU General Public
License <https://docs.moodle.org/dev/License>.

Moodle is written in PHP and JavaScript and uses an SQL database for storing
the data.

See <https://docs.moodle.org> for details of Moodle's many features.
