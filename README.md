This application contains..

APEX 
- Login page
- Register page
- Password reset page
- Request new password page
- User management 
_ Universal theme

Database
- Custom login functions 
- User management tables
- Registration and login functions
- Log functionalities 

* The PKG's are using email utilities of Oracle. 

User the below code to get your own usename/password.

declare
 
 l_user_name varchar2(100);
 l_user_pwd varchar2(100);
 
 begin
 l_user_name :='admin@apex-base.com';
 l_user_pwd  := APP_SECURITY_PKG.get_hash('admin@apex-base.com','Welcome01');
 
 UPDATE app_user
        SET
            usr_name = l_user_name,
            usr_pwd  = l_user_pwd
    WHERE
        usr_id = 1;

end;
