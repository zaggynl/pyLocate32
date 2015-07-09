Locate32 NOTES
'''
# sources:
# app I'm copying to linux: http://sourceforge.net/projects/locate32/?source=typ_redirect
# app I borrowed tray stuff from: http://kde-apps.org/content/show.php/CpuFreq+Tray?content=67720
# Qstuff: http://pyqt.sourceforge.net/Docs/PyQt4/qtgui.html
# Popen: http://stackoverflow.com/questions/2837214/python-popen-command-wait-until-the-command-is-finished
# Popen.communicate: https://docs.python.org/2/library/subprocess.html#subprocess.Popen.communicate
# threading: http://stackoverflow.com/questions/636561/how-can-i-run-an-external-command-asynchronously-from-python
# sudo: http://stackoverflow.com/questions/5191878/change-to-sudo-user-within-a-python-script
# shlex example: http://stackoverflow.com/questions/4091242/subprocess-call-requiring-all-parameters-to-be-separated-by-commas
# oldschool kill thread: https://web.archive.org/web/20130503082442/http://mail.python.org/pipermail/python-list/2004-May/281943.html
# freaking python garbage collection eats program after showing window: http://stackoverflow.com/questions/18061178/pyqt-window-closes-after-launch
# creating windows is odd: https://gist.github.com/justinfx/1951709
# more on window creation: http://www.learningpython.com/2008/09/20/an-introduction-to-pyqt/
# minimize to tray: https://stackoverflow.com/questions/758256/pyqt4-minimize-to-tray
# layout and widgets: https://stackoverflow.com/questions/8814452/pyqt-how-to-add-separate-ui-widget-to-qmainwindow
# design in qt creator, save, then convert to py file
# sudo apt-get install qtcreator pyqt4-dev-tools
# pyuic4 mainwindow.ui -o mainwindow.py
# http://pythonthusiast.pythonblogs.com/230_pythonthusiast/archive/1358_developing_cross_platform_application_using_qt_pyqt_and_pyside__gui_application_development-part_5_of_5.html
# pushbutton code for generated gui: https://stackoverflow.com/questions/11113247/how-does-one-make-a-button-in-the-main-window-open-a-different-window
# redirect output of subproces: https://stackoverflow.com/a/3247271
# string splitting: https://stackoverflow.com/questions/25253120/python-split-string-by-space-and-strip-newline-char#25253160
# dump variable:
#         from inspect import getmembers
#         from pprint import pprint
#         pprint(getmembers(output))
# dump variable to file
#         from inspect import getmembers
#         from pprint import pprint
#         logFile=open('mylogfile'+'.txt', 'w')
#         pprint(getmembers(dataobject), logFile)
#
# for open folder/open file menu: https://stackoverflow.com/questions/23993895/python-pyqt-qtreeview-example-selection
# handle KeyboardInterrupt: https://stackoverflow.com/questions/26893377/how-to-close-windows-in-pyqtgraph
# Another way: https://stackoverflow.com/questions/1112343/how-do-i-capture-sigint-in-python
# https://stackoverflow.com/questions/4938723/what-is-the-correct-way-to-make-my-pyqt-application-quit-when-killed-from-the-co
# definite way (NOT GRACEFUL): https://stackoverflow.com/a/6072360
# https://stackoverflow.com/questions/2963263/how-can-i-create-a-simple-message-box-in-python
# http://doc.qt.io/qt-4.8/qmessagebox.html
# get directory from full path: http://stackoverflow.com/questions/15022854/get-the-directory-path-of-absolute-file-path-in-python
# qmodelindex: http://stackoverflow.com/questions/25943153/how-to-access-data-stored-in-qmodelindex
# http://stackoverflow.com/questions/13564550/resizing-widgets-in-pyqt4
# http://www.qtforum.org/article/38989/how-to-make-qt-widgets-resize-automatically.html
# -> http://stackoverflow.com/a/21467559
# https://forum.qt.io/topic/19152/qlayout-attempting-to-add-qlayout/2
# http://stackoverflow.com/questions/1064335/in-python-2-5-how-do-i-kill-a-subprocess
# analyze segmentation fault: http://stackoverflow.com/a/10035594
# gdb python
# (gdb) run /path/to/script.py
# ## wait for segfault ##
# (gdb) backtrace
# # stack trace of the c code
#TODO

#DONE_get update command to work
#\show notifications for update success/failure
#DONE->make search screen
#\use QColumnView and QFileSystemModel instead of QTextBrowser for results
#fix
#QObject::connect: Cannot queue arguments of type 'QTextCursor'
#(Make sure 'QTextCursor' is registered using qRegisterMetaType().)
#http://www.qtforum.org/article/24502/gui-crash.html
#DONE\fix grey search button after search is done
#make settings screen
#make about screen
#make paths for kdesudo and updatedb variables and settings
#DONE_gksu/gksudo check
#DONE-fix main thread so you can use Ctrl+C to break
#DONE-don't show right click context menu on startup or no search results
#DONE-show search screen on doubleclick
#DONE-double check animation loop(when killing updatedb)
#DONE-clicking search sometimes generates Segmentation fault
#DONE-fix resizing and low res window looks
#DONE-ask if sure when searching for nothing (*)
#SIZE SORTS BY STRING, NOT BY INT-sort by filename/date created/size
# DONE- TRY http://www.linuxquestions.org/questions/programming-9/pyside-qtreewidget-numeric-sorting-4175502323/#post5156692
# DONE-fix ProxyModel(QSortFilterProxyModel) so we can get index to get stuff for context menu
#DONE-add Open with.. dialog
#-get Settings screen to work, start using conf file?
#-Ctrl+F in search window to search results?
#-proper way to kill updatedb thread, only kill our updatedb thread not every process updatedb
#-look into:
#       (during startup)
#       Bus::open: Can not get ibus-daemon's address.
#       IBusInputContext::createInputContext: no connection to ibus-d
#-look into:
#       #when building search list)
#       #QObject::connect: Cannot queue arguments of type 'Qt::Orientation'
#       (Make sure 'Qt::Orientation' is registered using qRegisterMetaType()
#-clean code
#
'''