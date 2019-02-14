
<center> Sunbird-Intl Documentation</center>


## What is Sunbird??

Sunbird is a societal learning platform built for cloud/mobile native environments and meant to address teaching and learning use cases.Multiple organizations can exist independently as tenants on the platform and users of these organizations can access the platform via mobile devices, laptops and desktops.

## Common Queries.

- Question:  Roles of content editor or content service (Content creator, reviewer etc.) and what actions those roles can do?

 <u>Answer</u>:    
          <center>User Roles and Respective Responsibilities</center>

|  User Role    | Content Creation | Review, Reject , & Publish | Upload Content | Other Actions |
|-------------------|---------------------|---------------------|-------------------------|-----------------|
| An **Organisation Administrator (Org admin)** manages the overall functioning and upkeep of the  organisation, and also define and manages user roles and permissions |       No       |       No       |  No | ✔️   <a href="features-documentation/#adminrole_matrix"> read more</a>
| A **System Administrator (Sys admin)** manages installation, configuration and operation of the system |       No       |       No       |  No | ✔️   <a href="features-documentation/#adminrole_matrix"> read more</a>
| A **Course Mentor** guides and instructs learners on how to undertake a course. They create batches of users to enrol for a course and ensure completion of a course within a stipulated time |       No       |       No       |  No | ✔️   <a href="features-documentation/userrole/#role-specific-responsibilites"> read more</a>~~       
| A **Content Reviewer** assesses  created content within prescribed guidelines | No | ✔️  | ✔️  | No 
| A **Teacher Badge Issuer** is responsible for assigning badges to teachers based on the discretion of the concerned organization | No | No | No | ✔️  <a href="features-documentation/userrole/#role-specific-responsibilites"> read more</a>
| A **Book Creator** curates and compiles books. Registered users become book creators when book creation rights are assigned to them | ✔️  (Only Books) | No | ✔️ | No 
|  A **Book Reviewer** assesses books within defined and prescribed guidelines| No | ✔️  (Only Books) | No | No
|A **Public** user is any user with registered credentials | No | No | No | ✔️  <a href="features-documentation/userrole/#role-specific-responsibilites"> read more</a>
| An **Announcement Sender** creates and sends announcements. The Announcement feature allows to send system wide messages to a target audience| No | No | No | ✔️  <a href="features-documentation/userrole/#role-specific-responsibilites"> read more</a>
| A **Content Creator** is a registered user with permission to create content | ✔️ (Collection, Course, Study Material, Lesson Plan) | No | ✔️ | No

<br/><br/>
- Question : Content publishing/workflow states???<br>
<u>Answer</u> : ```sequence
Draft->Review->Live/unlisted->flag(optional)```

<br/><br/>
- Question : Content authoring in collaboration. How it works? Can two users open the same content at the same time and edit?<br>
 <u>Answer</u> :  This Feature is still in devlopement Stage there is an Api call to Lock the content (params: userId,resourceId) and after making api call the content is locked for minimum 10 mins. and for content collaboration if two user(A,B) engaged in creating content then A will see his content in draft tab and B's content in collaboration tab.


<br/><br/>
- Question : Types of content supported<br/>
<u>Answer:</u>

``  Video (.mp4, .webm)
    HTML zip
    ECML (created using the inbuilt content editor)
    EPUB
    H5P
    Audio (.mp3)
    Images (.jpeg, .png)
    Document format (.pdf)
    URLs of YouTube videos and other files
    URLs of other externally hosted content``
    
<br/><br/>
- Question : How to tag content? <br>
<u> Answer </u> : In a portal there is a wokspace section. so while creating resource we can specify the keywords in    `Keyword` field ,the keywords must be the words which are related to the resource. <br>
- Question : How content gets flagged as inappropriate etc?<br>
<u> Answer </u> : In a content lifecycle we have a flag as a staus in which if a content is inappropriate ,the project manager  can flag that content. after that content will dissappear.<br>
- Question : Permissions control? <br>
<u> Answer </u> : 
Based on user responsibilities, rights are provided to: 

- create 
- review 
- publish 
- consume

Specific users are granted administration rights to manage users or organization profile creation, onboarding, deletion, passwords, and site look-and-feel customization.Based on user responsibilities, rights are provided.<br>

<br/>
- Question : How the plagiarism works? <br>
<u> Answer </u> : Currently the plagiarism is not been in action with the following version relaesed.<br>

<br/><br/>
- Question : Constraints like maximum size of the content allowed and how to increase that?<br>
<u> Answer </u> :The platform supports:<br>

Content / File type |Maximum File Size (for single file)
--------------------|-----------------------------------
Book,Course,Collection,Lesson Plan | 250 MB
HTML (as zip files) |50 MB
EPUB | 50 MB
H5P |50 MB
Video (.mp4, webm) | 25 MB
.pdf | 25 MB <br>

But this size is just a backend configuration we can change it easily.<br>
<br/>
- Question : Content export options ? <br>
<u> Answer</u> : There is a script by running we can export our content from global enviroment to local enviroment. but this                   is a occasional activity and this option is not availaible to every user.<br>

<br/>
- Question : Bulk authoring of content – How is it done? How to author questions? How to author assessments?<br>
<u> Answer </u> : 
To bulk upload content,

1. Send a mail to info@sunbird.org, with the subject as  request to bulk upload 
2. Supported file formats:

	- Text (.pdf)
    	- Video (.mp4, .webm, YouTube URLs)
    	- HTML 
    	- ECML (created using the inbuilt content editor)
    	- EPUB
    	- H5P
	
3. File size should not exceed 25MB per file
4. The team will respond with  a form (excel file), seeking basic information on the nature of the content
5. Reply to the mail after filling in the required details, such as file name, description, file type, subject, class 
6. This information will be used as metadata for each file. Metadata is important to make content searchable and usable by platform members
7. Compress  all the content files into one .zip file. The size of the zip file should not exceed 25MB  
8. Upload the .zip file on Google drive and share the link with or email the zipped folder to info@sunbird.org
9. Ensure the following if the content is URL based:
	
	- The destination website uses HyperText Transfer Protocol Secure (https) and not  HyperText Transfer Protocol (http). 
	- The destination website is enabled for cross origin resource sharing 

	***Note:***
	
    Before sharing the .zip file, check that every author, or content creator is a registered user on the platform. To register on the platform, share your details at info@sunbird.org. All content that is  uploaded will be added with  the creator’s credentials
10. On receiving the .zip file, the Content PMU will review it before it is uploaded 
11. The status of all  content uploaded in bulk  will  be  ‘Draft’
12. The system sends an email alert to the organization’s designated reviewers 
13. On reviewing the content, the reviewer either accepts or rejects it
14. On accepting the content, the reviewer clicks Publish, to make the content live on the platform<br>
and for authoring questions(mcq's) we can easily do that from the ui itself<br>

<br/>
- Question : ML based content curation – How it works?<br>
<u> Answer </u> : We can tag content with specific keywords the techniques used is Deep Learning ,LSTM(Long short term memory) which give the respective content as a result  after performing any query search relaveant to any subject. and this model uses reinforcement learning which takes feedback of the result and improves the model for better search  results.<br> 
- Question :  How to generate QR codes. How to edit QR codes or DIAL codes <br/>
<u>Answer:</u>  Dial code creation require API access. Ask the team to enable access to your api-key. 
Use APIs to -<br/> ```Create publisher>Generate dial code>Update dial code and publisher>Publish dial code>Link dial code ```


    <br/>
- Question : Number of plugins available <br/>
<u>Answer: The plugins available currently are 66 </u>  


<br/>

- Question : How to enable a plugin <br/>
<u>Answer</u>: TBD 

<br/>
 
- Question : Development effort involved to develop a plugin <br/>
<u>Answer</u> :  tbd
    
    
