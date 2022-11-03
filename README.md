Liza Stolce

CarSHAiR QA Assessment

—————————————————————

Defect 1 :  Search Page > Notes not opening (Error 404)

Preconditions: 
the User (authorized or unauthorized) is on the Search page;
at least 1 Note preview is visible.

Steps: 
1. User clicks on the first note preview.

Expected Result:   the Note is open

Actual Result:   the error 404 page is open: This page could not be found

—————————————————————

Defect 2 :  Search Page > Search by Owner does not work correctly

Defect 2 note: since this is a test assignment we have only one user for all notes. This makes it difficult to identify the bug as we are not able to test with different users. Therefore, in this test, we use a user with a deliberately incorrect email


Preconditions: 
the User (authorized or unauthorized) is on the Search page;
	
Steps: 
1. count the number N1 of messages visible on the page;
2. enter incorrect user email ‘tester@gma.com’  in the Search by Owner field;
3. count the number N2 of messages visible on the page

Expected Result:   no Note preview visible;   N2 == 0 or N2 < N1

Actual Result:all notes that were visible before passing the test are visible;  N2 == N1

—————————————————————

Defect 3 :  Search Page > Using the Search by Owner interferes with the Search by Text

Preconditions: 
the User (authorized or unauthorized) is on the Search page;
	
Steps:
1. count the number N1 of messages visible on the page;
2. enter valid email ‘tester@shair.co’  in the Search by Owner field;
3. enter text ‘sample note’ in the Search by Text field
4. count the number N2 of messages visible on the page

Expected Result:   N2 < N1

Actual Result:   N2 == N1

—————————————————————

Defect 4 :  Profile Page > No possibility to Add a large Note (about 500 characters)

Preconditions: 
the authorized User is on the Profile page; 
bigNoteText is:  
Lorem ipsum dolor sit amet. Eos eaque dicta et omnis deleniti quo quis recusandae qui ipsam galisum aut dolore asperiores hic accusamus expedita. A molestias suscipit et debitis atque qui dolorem cumque et expedita eveniet cum pariatur laborum. Qui delectus autem ut laboriosam corrupti nam similique galisum ut voluptas doloremque qui labore voluptates sit itaque expedita et dignissimos ratione. Qui sunt veniam et velit nisi a tempore esse et mollitia illum id voluptatibus autem sed voluptatibus dignissimos.
	
Steps: 
1. put the bigNoteTex in the Note Content field
2. click the Submit button
	
Expected Result:   the note appears in Previous Notes

Actual Result:   the note does not appear in Previous Notes

—————————————————————

Defect 5 :  Profile Page > No message about note size limits

Preconditions: 
the authorized User is on the Profile page;
bigNoteText is:  
Lorem ipsum dolor sit amet. Eos eaque dicta et omnis deleniti quo quis recusandae qui ipsam galisum aut dolore asperiores hic accusamus expedita. A molestias suscipit et debitis atque qui dolorem cumque et expedita eveniet cum pariatur laborum. Qui delectus autem ut laboriosam corrupti nam similique galisum ut voluptas doloremque qui labore voluptates sit itaque expedita et dignissimos ratione. Qui sunt veniam et velit nisi a tempore esse et mollitia illum id voluptatibus autem sed voluptatibus dignissimos.

Steps: 
1. put the bigNoteTex in the Note Content field

Expected Result: 
the Submit button not active or a Warning message about the limit of characters appears 

Actual Result:  the Submit button is active and Limit Warning message does not appear

—————————————————————

Defect 6 :   No way to edit note:

Preconditions: 
the Authorized User is on the Profile page;
at least 1 Note preview is visible

Steps:
1. user clicks on the first note preview 
2. the note is open

Expected Result:   the options to edit the note exist

Actual Result:   the options to edit the note does not exist


--------------------------------------------

    Note: there was still such a defect, but apparently it was fixed on 11/2:

Defect, FIXED:   No option to Logout

Steps: 
1. the Authorized User is on the Profile page.

Expected Result:   Logout option exists.

Actual Result:   no option to Logout

