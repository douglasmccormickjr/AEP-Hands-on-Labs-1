Lab 3.1 - Build a Student Performance schema (ExperienceEvent)
==========
<table style="border-collapse: collapse; border: none;" class="tab" cellspacing="0" cellpadding="0">

<tr style="border: none;">

<div align="left">
<td width="600" style="border: none;">
<table>
<tbody valign="top">
      <tr width="500">
            <td valign="top"><h3>Objective:</h3></td>
            <td valign="top"><br>This long lab will show you how to construct 
            </td>
     </tr>
     <tr width="500">
           <td valign="top"><h3>Prerequisites:</h3></td>
           <td valign="top"><br>none
           </td>
     </tr>
</tbody>
</table>
</td>
</div>

<div align="right">
<td style="border: none;" valign="top">

<table>
<tbody valign="top">
      <tr>
            <td valign="middle" height="70"><b>section</b></td>
            <td valign="middle" height="70"><img src="https://github.com/adobe/AEP-Hands-on-Labs/blob/master/assets/images/left_hand_nav_menu_schemas.png?raw=true" alt="Identities"></td>
      </tr>
      <tr>
            <td valign="middle" height="70"><b>version</b></td>
            <td valign="middle" height="70">1.0.1</td>
      </tr>
      <tr>
            <td valign="middle" height="70"><b>date</b></td>
            <td valign="middle" height="70">2020-01-06</td>
      </tr>
</tbody>
</table>
</td>
</div>

</tr>
</table>

Instructions:
-----------------
1. In the left-hand menu, navigate to "Schemas"
2. Click "Create Schema"
3. Click on "Untitled Schema" (either place)
4. In the right-hand menu, name it "Student Performance Schema 001 <your-initials>" (Description is purely optional)
5. In the left-hand schema composition menu, click on the "Assign" button across from Class
6. Here's where you can choose your base level schema behavior:

     - Time-based Events (ExperienceEvent)
     - Customer Snapshots (Profile)

7. In this example, choose "XDM ExperienceEvent" and click "Assign class"
     Note: you cannot have a schema that does both ExperienceEvent and Profile at the same time -- this due to the nature of how the Unified Profile Service stitches data
8. In the left-hand schema composition menu, click on the class "XDM ExperienceEvent"
9. Below that area, click on the "Add" button across from "Mixins"
10. Here's where you can build your own Mixin or use a prior/similar Mixin object that conforms to your data.
11. Click on a few "Adobe" pre-built Mixin and select the "Preview mixin structure" option on the right-hand side to see it's contents
     Note: please don't add any of these pre-built mixins
12. In this lab, we'll create a new Mixin from scratch.  Click "Create new mixin" on the very top
13. Display name is "Student Performance Mixin 001 <your-initials>"
14. Notice that "timestamp" is a required field appended to the base level of the schema-- this is intensional since this is where each timestamp needs to be provided for each record
15. In the left-hand schema composition menu, click on your newly create Mixin (it should be highlighted now)
16. ***Finally the good stuff*** here's where we add items/fields to the schema that correspond to the file or table we'll be pushing up into AEP
17. You have the "option" to create an Object data-type where other values/data-fields are children to the Object.  This is helpful in certain operations such as this:

    Test Performance Data Mixin
        Test Type
        Test Length
        Test Score Indexed
        Test Version

   Tester Information Mixin
        Student Number
        Student Name
        Testing Date

This object heirarchy could help keep certain aspects of the data better organized and menued-- but this isn't a requirement.

For this lab, you'll create a new top level object called "StudentTest", here's how

19. Click "Add Field"
20. Rename to "StudentTest"
21. On data-type dropdown, select "Object"
22. Scroll to the very bottom and hit save
23. Form that object, select "Add Field" -- before you do that, please review the raw data first before you create these new fields
24. Goto this URL https://www.mockaroo.com/schemas/209787
25. Change the first string ```crmid:132145##``` to your assigned value (ask the instructor)
26. Generate your new file (this will be the data you'll be uploading into AEP)
27. Finish adding your fields and save this schema
 
<br>
<br>
<br>
