
![image](https://user-images.githubusercontent.com/91851332/156097601-89be5981-3621-4433-9981-c3f03df3a713.png)


### Create user

aws iam create-user --user-name test123

### Create password for user

aws iam create-login-profile --user-name test123 --password Test@123




### Use the create-user command to create the user.

$ aws iam create-user --user-name MyUser

### To create an IAM group and add a new IAM user to it

    Use the create-group command to create the group.

$ aws iam create-group --group-name MyIamGroup





### Use the add-user-to-group command to add the user to the group.

$ aws iam add-user-to-group --user-name MyUser --group-name MyIamGroup

### To verify that the MyIamGroup group contains the MyUser, use the get-group command.

$ aws iam get-group --group-name MyIamGroup



###  The following command uses create-login-profile to set an initial password on the specified user. 

When the user signs in for the first time, the user is required to change the password to something that only the user knows.

$ aws iam create-login-profile --user-name MyUser --password My!User1Login8P@ssword --password-reset-required

### You can use the update-login-profile command to change the password for an IAM user.

$ aws iam update-login-profile --user-name MyUser --password My!User1ADifferentP@ssword



### You can use the create-access-key command to create an access key for an IAM user. 

An access key is a set of security credentials that consists of an access key ID and a secret key.

An IAM user can create only two access keys at one time. If you try to create a third set, the command returns a LimitExceeded error.


$ aws iam create-access-key --user-name MyUser
