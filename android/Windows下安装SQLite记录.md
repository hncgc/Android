# Windows下安装SQLite记录

Windows下安装SQLite
---

[SQLite 安装](https://www.runoob.com/sqlite/sqlite-installation.html)  

~~~
https://www.sqlite.org/download.html

在 Windows 上安装 SQLite
请访问 SQLite 下载页面，从 Windows 区下载预编译的二进制文件。

您需要下载 sqlite-tools-win32-*.zip 和 sqlite-dll-win32-*.zip 压缩文件。

创建文件夹 C:\sqlite，并在此文件夹下解压上面两个压缩文件，将得到 sqlite3.def、sqlite3.dll 和 sqlite3.exe 文件。

添加 C:\sqlite 到 PATH 环境变量，最后在命令提示符下，使用 sqlite3 命令，将显示如下结果。

C:\>sqlite3

sqlite-dll-win64-x64-3330000.zip (809.89 KiB)		64-bit DLL (x64) for SQLite version 3.33.0.
(sha3: 1b078c320adb1d9ff57c508eb0d2ef05bf13ca2e9cbb37c2ea72099373cdfd61)

sqlite-tools-win32-x86-3330000.zip (1.76 MiB)		A bundle of command-line tools for managing SQLite database files, including the command-line shell program, the sqldiff.exe program, and the sqlite3_analyzer.exe program.
(sha3: 5b13a53afe89ca0a975f0c166d5e4c33c83695ceea75ae297f5471df3adde4b0)

D:\>cd sqlite

D:\SQLite>

2020/09/07  12:42    <DIR>          .
2020/09/07  12:42    <DIR>          ..
2020/08/14  21:44           521,728 sqldiff.exe
2020/09/07  12:40           500,989 sqlite-dll-win32-x86-3330000.zip
2020/09/07  12:37           829,331 sqlite-dll-win64-x64-3330000.zip
2020/09/07  12:37         1,844,004 sqlite-tools-win32-x86-3330000.zip
2020/08/15  05:15             6,262 sqlite3.def
2020/08/15  05:15         1,950,208 sqlite3.dll
2020/08/14  21:45           987,136 sqlite3.exe
2020/08/14  21:44         2,037,248 sqlite3_analyzer.exe
               8 个文件      8,676,906 字节
               
 D:\SQLite 的目录

2020/09/07  13:22    <DIR>          .
2020/09/07  13:22    <DIR>          ..
2020/08/14  21:44           521,728 sqldiff.exe
2020/08/15  05:15             6,262 sqlite3.def
2020/08/15  05:15         1,950,208 sqlite3.dll
2020/08/14  21:45           987,136 sqlite3.exe
2020/08/14  21:44         2,037,248 sqlite3_analyzer.exe
               5 个文件      5,502,582 字节
               2 个目录 200,454,516,736 可用字节


D:\SQLite>sqlite3
SQLite version 3.33.0 2020-08-14 13:23:32
Enter ".help" for usage hints.
Connected to a transient in-memory database.
Use ".open FILENAME" to reopen on a persistent database.
sqlite> .help
.archive ...             Manage SQL archives
.auth ON|OFF             Show authorizer callbacks
.backup ?DB? FILE        Backup DB (default "main") to FILE
.bail on|off             Stop after hitting an error.  Default OFF
.binary on|off           Turn binary output on or off.  Default OFF
.cd DIRECTORY            Change the working directory to DIRECTORY
.changes on|off          Show number of rows changed by SQL
.check GLOB              Fail if output since .testcase does not match
.clone NEWDB             Clone data into NEWDB from the existing database
.databases               List names and files of attached databases
.dbconfig ?op? ?val?     List or change sqlite3_db_config() options
.dbinfo ?DB?             Show status information about the database
.dump ?TABLE?            Render database content as SQL
.echo on|off             Turn command echo on or off
.eqp on|off|full|...     Enable or disable automatic EXPLAIN QUERY PLAN
.excel                   Display the output of next command in spreadsheet
.exit ?CODE?             Exit this program with return-code CODE
.expert                  EXPERIMENTAL. Suggest indexes for queries
.explain ?on|off|auto?   Change the EXPLAIN formatting mode.  Default: auto
.filectrl CMD ...        Run various sqlite3_file_control() operations
.fullschema ?--indent?   Show schema and the content of sqlite_stat tables
.headers on|off          Turn display of headers on or off
.help ?-all? ?PATTERN?   Show help text for PATTERN
.import FILE TABLE       Import data from FILE into TABLE
.imposter INDEX TABLE    Create imposter table TABLE on index INDEX
.indexes ?TABLE?         Show names of indexes
.limit ?LIMIT? ?VAL?     Display or change the value of an SQLITE_LIMIT
.lint OPTIONS            Report potential schema issues.
.load FILE ?ENTRY?       Load an extension library
.log FILE|off            Turn logging on or off.  FILE can be stderr/stdout
.mode MODE ?TABLE?       Set output mode
.nullvalue STRING        Use STRING in place of NULL values
.once ?OPTIONS? ?FILE?   Output for the next SQL command only to FILE
.open ?OPTIONS? ?FILE?   Close existing database and reopen FILE
.output ?FILE?           Send output to FILE or stdout if FILE is omitted
.parameter CMD ...       Manage SQL parameter bindings
.print STRING...         Print literal STRING
.progress N              Invoke progress handler after every N opcodes
.prompt MAIN CONTINUE    Replace the standard prompts
.quit                    Exit this program
.read FILE               Read input from FILE
.recover                 Recover as much data as possible from corrupt db.
.restore ?DB? FILE       Restore content of DB (default "main") from FILE
.save FILE               Write in-memory database into FILE
.scanstats on|off        Turn sqlite3_stmt_scanstatus() metrics on or off
.schema ?PATTERN?        Show the CREATE statements matching PATTERN
.selftest ?OPTIONS?      Run tests defined in the SELFTEST table
.separator COL ?ROW?     Change the column and row separators
.sha3sum ...             Compute a SHA3 hash of database content
.shell CMD ARGS...       Run CMD ARGS... in a system shell
.show                    Show the current values for various settings
.stats ?on|off?          Show stats or turn stats on or off
.system CMD ARGS...      Run CMD ARGS... in a system shell
.tables ?TABLE?          List names of tables matching LIKE pattern TABLE
.testcase NAME           Begin redirecting output to 'testcase-out.txt'
.testctrl CMD ...        Run various sqlite3_test_control() operations
.timeout MS              Try opening locked tables for MS milliseconds
.timer on|off            Turn SQL timer on or off
.trace ?OPTIONS?         Output each SQL statement as it is run
.vfsinfo ?AUX?           Information about the top-level VFS
.vfslist                 List all available VFSes
.vfsname ?AUX?           Print the name of the VFS stack
.width NUM1 NUM2 ...     Set minimum column widths for columnar output
sqlite>

sqlite> .show
        echo: off
         eqp: off
     explain: auto
     headers: off
        mode: list
   nullvalue: ""
      output: stdout
colseparator: "|"
rowseparator: "\n"
       stats: off
       width:
    filename: :memory:
sqlite>

sqlite> .quit


~~~
