# Frequently Asked Questions

A place to have questions and solutions.

#### 1. **Q:** On MacOS double and single quotes are replaced by invalid characters, how to fix?

   **A:** You have to disable auto-correction in MacOS System Preferences. See [Issue #1949](https://github.com/robotframework/RIDE/issues/1949)

#### 2. **Q:** In the newest versions of RIDE (1.7.4) and with Robot Framework 3.1.2, when I edit a Test Suite having `: FOR`, then, when is executed, appears the following error: `FOR loop contains no keywords.`. How to fix this?

   **A:** Robot Framework is tolerant to the old `: FOR` format, and the test suite can be executed correctly. However, when the file is edited in RIDE, it looses the old style formatting, so you must add the terminating `END`.

   In the next images you can see how is shown the old and new styles (the Code Editor is showing the file not formatted):
   
   ![Old FOR in Text Editor](https://robotframework.transformidea.com/RIDE/images/Old_style_Text_View.png)
   ![Old FOR in Grid Editor](https://robotframework.transformidea.com/RIDE/images/Old_style_Grid_Editor_View.png)
   
   Then it must be changed to:
   ![New FOR in Text Editor](https://robotframework.transformidea.com/RIDE/images/New_style_Text_View.png)
   ![New FOR in Grid Editor](https://robotframework.transformidea.com/RIDE/images/New_style_Grid_Editor_View.png)

#### 3. **Q:** I installed RIDE, on Python 3.7 but it does not start, see below the error. How to start RIDE?

    ```
    C:\>ride
    Traceback (most recent call last):
      File "C:\Program Files\Python37\Scripts\ride.py", line 21, in <module>
        from robotide import main
    ImportError: No module named robotide
    ```

   **A:** A possible way to start RIDE is:
 
   `python -m robotide.__init__`

   You can then go to `Tools>Create RIDE Desktop Shortcut`, or run the shortcut creation script with:
 
   `python -m robotide.postinstall -install`
 
#### 4. **Q:** How can I preserve the _Log.html_ and _Report.html_ from different test runs, preferably with a timestamp?

   **A:** You should use the `robot` option for the output directory (`-d`) in the arguments text field. See 
[Issue #1891](https://github.com/robotframework/RIDE/issues/1891)

   See below an example for Windows, using date formatting in the current test directory:

   `-d ./%date:~-4,4%%date:~-10,2%%date:~-7,2%`

   The similar result in Linux or MacOS can be obtained with the `date` command:

   ```
   -d `date +%F_%X`
   ```