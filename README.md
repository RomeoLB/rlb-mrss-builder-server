# rlb-mrss-builder-server
Node application to build a Video/Image MRSS feed and serve it from a Brightsign player

This application allows the user to upload image and video files to a specific folder via the player DWS (Diagnostic Web Server) and then from a control page specify the display time for displaying the images and then generate the MRSS feed to be served locally with the click of a couple of buttons.  

### Who would want to use this application?:

- Users who do not want to use BrightAuthor (after the initial publish) for content update
- Users who just want to upload and delete files from a folder for content update
- Users who want to setup a MRSS builder/server but who don't know how or can't be bothered to do so ( https://docs.brightsign.biz/space/DOC/2036105242/Developers)

### How to get started:

1. Download and unzip the content of mrss-builder-server-bs.zip file to a blank SD card.
2. Insert the SD card with the unziped file in a Brightsign player (whilst thepower connector is unplugged)
3. Insert the power connector in the player and wait for the player to display at the bottom of the screen the URL for the control page
   
   <img width="848" alt="image" src="https://github.com/user-attachments/assets/3268b618-7f2b-4ead-b3ee-efe09e8bcda7">
   
5. Using a web browser enter the URL that is displayed at the bottom of the player screen
   
   <img width="967" alt="image" src="https://github.com/user-attachments/assets/7977eb0d-3461-447c-8a2f-4d6959c59674">
   
7. Whilst on the control page enter a number between 1-999 (display time for image  to be entered even if there will be no images in te MRSS feed) in the textfield, click on the "Set" button then on the "Update" button to generate the first MRSS feed on the Brightsign device
   
   <img width="915" alt="image" src="https://github.com/user-attachments/assets/47ced427-d047-4bf1-8e93-b582596a6015">
   
9. Enter the URL that was displayed at the top of the screen on step 3 to check if the MRSS feed has been build and is indeed available from the expexted endpoint (as per the below example)
    
   <img width="946" alt="image" src="https://github.com/user-attachments/assets/58814c16-d498-4b8f-9113-7c23e8ad2a35">
   
11. Create a Brightauthor:Connected presentation and add a "Live Feed" state to the playlist and insert the local MRSS feed URL under State Properties > Source > URL, then publish the presentation
 
   <img width="770" alt="image" src="https://github.com/user-attachments/assets/97c71512-948c-40d9-9d77-d4c1ac181ada">

Once the presentation is published you will be able to update the presentation content without the need to republish the presentation or even open BrightAuthor again.

### How do I update the MRSS feed Content?

1. Access the player Local DWS by entering the player's IP address
2. Click on SD tab then Browse to the "NodeApp/public/media" folder. From that folder you can delete and upload new video and image files.

<img width="1004" alt="image" src="https://github.com/user-attachments/assets/3ee34fa4-9ccf-466f-90c5-0c2cd39d4c59">

3. Navigate to the control page (repeat steps 4 and 5 from the "How to get started" section) to regenerate the update MRSS feed with the newly uploaded files. 



