# SOFFG backend build

steps:
1. open the project
2. switch into master branch
3. update the project
4. build the project (gradle -> build)
5. go to application.properties file and comment out whether you are going to deploy UAT or PROD
6. before start building goto build folder and delete it
7. goto gradle tab and double click war tab
8. you can see build folder has been created
9. If you go to lib section you can see .war file has been genarated 

# SOFFG Frontend build

steps:
1. goto master branch
2. update the project
3. delete www folder
4. in terminal run " ng build " command

# SOFFG backend deployment

1. goto s3 bucket
2. goto soffcricket (you can see prod and uat sections)
3. goto uat or prod
4. goto backup-war
5. create a folder
6. go back to uat/prod section
7. goto latest-war file 
8. select the war file -> actions -> move -> browse S3 -> uat -> backup-war/ -> new folder that u created -> choose destination -> move
9. in latest war file ; upload -> add file -> goto local repo envirenment -> build -> lib -> select the war file -> open -> upload
10. backend deployment has done

# SOFFG frontend deployment

1. goto backup-ui
2. create a folder with name as date
3. go back to uat/prod
4. latest-ui
5. select all but unchecked deploykey.txt file (dont copy it )
6. actions -> move -> choose backup-ui destination -> move
7. delete the deploykey.txt file in latest-ui ( which you unmoved )
8. in latest-ui file
9. upload -> add file -> goto local repo -> www -> select all ( dont select the folders ) -> open -> add folder -> select the folder (assets) -> upload
10. in your project folder create a deploykey.txt file and upload it to the latest-ui file again



#### https://442931939449.signin.aws.amazon.com/console ###
