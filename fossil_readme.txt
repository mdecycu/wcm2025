# Fossil SCM Sqlite database

fossil sql -R foo.fossil

進入 sqlite 指令環境後, 可以利用 .schema user 查驗 user 資料表的欄位設計.

以 select login, pw, info, cap from user;

可以查詢目前 foo.fossil 檔案中 user 資料表 login, pw, info 與 cap 等3個欄位的資料內容.

若要更改特定 login 登入帳號的 pw 或 cap 可以使用下列 sqlite3 SQL 語法:

update user set pw='mynewpassword' where login='myloginaccount';

update user set cap='s' where login='myloginaccount';

# Fossil SCM server

c:\repo for multiple .fossil files, c:\repo\wcm2025.fossil can be open to c:\repo\wd\wcm2025 with c:\repo\wd\wcm2025>fossil open ./../../wcm2025.fossil

fossil server c:\repo --notfound wcm2025

