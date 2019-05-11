# Wish List

## Features we would like to have in RIDE

1. Better Text Editor
    * Possibly embed external editor (or grab some code from good editors)
    * Including a toolbar
    * Better search and replace functions
2. Plugin for version control (SVN, GIT, ...)
3. Graphical Modeling of Test Suites / Test Cases
4. Plugin to assist with Pybot/Rebot command options
5. [Context-menu to open folder in OS file browser](https://github.com/robotframework/RIDE/issues/1650)
6. Auto-detect plugins installed with "pip install", without having to copy scripts into a certain folder
7. Restore tree-state (expanded, checkmarks) on reload-because-file-changed
8. Add log manager tab to manage and easy view of previous run logs in tabular format.. 
9. Run Test (F8) button (which is after "Search Tests (F3)" at top side) should support max 4 parallel runs. 
     * User can run 4 parallel run one after one.
     * Live run status in run tabs like run1, run2, run3 and run4.   
     * by this we can reduce multiple ride windows for multiple runs 

## Grid features:

1. Grid Editor Settings
     * Default column size: Used as minimum and maximum size for all columns in grid
     * Auto size columns:
          * Checked - Size will be calculated based on the longest text on that that column
          * Unchecked - Default column size will be used instead
     * Max column size: 
          * Used to force a maximum size when `Auto size columns` option is checked
          * Text that exceeds this size will either be wrapped or cut from view
     * Word wrap and auto size rows:
          * Checked - Text will be wrapped on multiple lines and row height will adapt to fit all lines
          * Unchecked
               * Text will be cut from view when it exceeds `Max column size`
               * Row height will fit only one line of text
2. Use cases and how grid should react
     * Changing font size should refresh grid and cause row and columns sizes to be recalculated
     * Cutting, pasting, inserting, commenting one or multiple cells should cause grid to recalculate sizes
     * `Default column size` should be enforced as minimum size when manually changing the column size (except when `Auto size columns` option is checked)
     * Word wrap will work by splitting text on multiple lines, even when text doesn't contain whitespaces

## Bugs we would like fixed in RIDE

1. [Don't spew warnings when we forget to use register_run_keyword](https://github.com/robotframework/ride/issues/1661) ([PR](https://github.com/robotframework/ride/issues/1662))