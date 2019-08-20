# Frequently Asked Questions

A place to have questions and solutions.

1. **Q:** On MacOS double and single quotes are replaced by invalid characters, how to fix?

   **A:** You have to disable auto-correction in MacOS System Preferences. See [Issue #1949](https://github.com/robotframework/RIDE/issues/1949)

2. **Q:** In the newest versions of RIDE (1.7.4) and with Robot Framework 3.1.2, when I edit a Test Suite having `: FOR`, then, when is executed, appears the following error: `FOR loop contains no keywords.`. How to fix this?

   **A:** Robot Framework is tolerant to the old `: FOR` format, and the test suite can be executed correctly. However, when the file is edited in RIDE, it looses the old style formatting, so you must add the terminating `END`.
   In the next images you can see how is shown the old and new styles (the Code Editor is showing the file not formatted):
   <placeholder for Old_style_Text_View.png>
   <placeholder for Old_style_Grid_Editor_View.png>
   Then it must be changed to:
   <placeholder for New_style_Text_View.png>
   <placeholder for New_style_Grid_Editor_View.png>



