# CJDBM

an DLL to use Mysql With C# project's

# How to

1- add the dll's to you project.

2- include the class by adding .

      using MySql.Data.MySqlClient;
      using CJ_DBM;
      
3- Make new database connection by calling the class cjdbm.
    cjdbm obj = new cjdbm("ServerURL","Server_UserName","Server_Password","Dadabase_Name");
    
4- The class Function's
    
    1- Open() 
      this function use to open database connection and must be called before the other functions
    2- query()
      this one for making a database query ! and Because I have used the mysql prepared statements to avoid SQL_INJECTION
      you will need to send parameter instead of values in the query
      Ex:
      obj.query(SELECT * FROM emp WHERE usr=@usr);
    3- bind()
      the one is for Bind parameters !
      it can pass one parameter at time so you need to call it if you have more than one param.
      Ex:
      obj.bind("@usr",Textbox1.Text);
    4- exe()
      this fucntion use to Execute the query with No return
    5- resultset()
      this fucntion use to Execute the query and return an array of the result as MysqlDateReader DataType !

