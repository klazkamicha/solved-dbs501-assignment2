Download Link: https://assignmentchef.com/product/solved-dbs501-assignment2
<br>
Write the code for the Procedure called <strong>modify_sal </strong>that will search table Employees and for a given Department Id  perform the following:

By using Cursor For Loop you will scan each employee’s salary and figure out is it smaller than the Average amount earned in that department (ignore the Commission) and then if YES adjust his/her salary to that average amount.  Count  # of employees who received salary increase. Do NOT perform unnecessary calculations in the loop. Also, be sure that you locked all rows before performing your Update  — you do NOT want to wait for just one row in the middle of your salary modification.

You also need to take care of the wrong input (Department Id is invalid) and also if that Department is empty (NO employees  there).   Then UNDO your change.




<u>Here are the possible outputs:</u>

SQL&gt; @a2-1;




Procedure created.

No errors.




SQL&gt; EXECUTE modify_sal(99);

This Department Id is invalid: 99




PL/SQL procedure successfully completed.




SQL&gt; EXECUTE modify_sal(190);

This Department is EMPTY: 190




PL/SQL procedure successfully completed.




SQL&gt; EXECUTE modify_sal(10);

No salary was modified in Department: 10




PL/SQL procedure successfully completed.




SQL&gt; EXECUTE modify_sal(110);

Employee William Gietz just got an increase of $1850

Total # of employees who received salary increase is: 1




PL/SQL procedure successfully completed.




SQL&gt; EXECUTE modify_sal(60);

Employee David Austin just got an increase of $960

Employee Valli Pataballa just got an increase of $960

Employee Diana Lorentz just got an increase of $1560

Total # of employees who received salary increase is: 3




PL/SQL procedure successfully completed.




SQL&gt; Rollback;

Rollback complete.




<ol start="2">

 <li>Write the code for the Function called <strong>Total_Cost</strong> that will for a provided Student Id return Total Cost for ALL enrolled courses. Test your Function for  a Valid and Invalid input by using BIND variables. You need to take care of an Invalid Id (returned value will be -1) and also if student is enrolled in NO courses (meaning the returned value will be 0).</li>

</ol>

Show all 3 tests with Bind variables as well.




<u>Here are the outputs:  </u>




If you enter 194 then

<table width="90%">

 <tbody>

  <tr>

   <td colspan="4"><strong>COST </strong></td>

  </tr>

  <tr>

   <td colspan="4">1195</td>

  </tr>

  <tr>

   <td colspan="4"></td>

  </tr>

  <tr>

   <td colspan="2"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

  <tr>

   <td width="3"></td>

   <td width="314"></td>

   <td width="314"></td>

   <td width="2"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>

If you enter 294 then

<table width="90%">

 <tbody>

  <tr>

   <td colspan="3"><strong>COST </strong></td>

  </tr>

  <tr>

   <td colspan="3">0</td>

  </tr>

  <tr>

   <td colspan="3"></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td width="3"></td>

   <td width="628"></td>

   <td width="2"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>

If you enter 494 then

<table width="90%">

 <tbody>

  <tr>

   <td colspan="2"><strong>COST </strong></td>

  </tr>

  <tr>

   <td colspan="2">-1</td>

  </tr>

  <tr>

   <td colspan="2"></td>

  </tr>

  <tr>

   <td width="317"></td>

   <td width="316"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>




3)   A) Write the Package Specification called <strong>My_pack </strong> for both OBJECTS created here.

<ol>

 <li>B) Then write the Package Body specification and compile without warnings.</li>

 <li>C) Test your Package by providing input as for Question 2)</li>

</ol>




4)    Now OVERLOAD your Package with TWO NEW variations of Function Total_Cost:




<ol>

 <li>First will accept TWO Input parameters: First Name and Last Name, returns Total Cost</li>

 <li>Second will accept ONE Input parameter: Zip Code (here you need a For Cursor Loop) it  returns Total Cost for ALL students living in the provided ZIP area</li>

 <li>C) Test your OVERLOADED Function in both forms from — by Full Name and by Zip input by  providing proper parameter values through BIND variables. Show your testing.</li>

</ol>

<u> </u>

<u>Here are the outputs:</u>




If you enter VERONA  GRANT  then

<table width="90%">

 <tbody>

  <tr>

   <td colspan="3"><strong>COST </strong></td>

  </tr>

  <tr>

   <td colspan="3">1195</td>

  </tr>

  <tr>

   <td colspan="3"></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td width="3"></td>

   <td width="628"></td>

   <td width="2"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>

If you enter YVONNE WINNICKI then

<table width="90%">

 <tbody>

  <tr>

   <td colspan="3"><strong>COST </strong></td>

  </tr>

  <tr>

   <td colspan="3">0</td>

  </tr>

  <tr>

   <td colspan="3"></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td width="3"></td>

   <td width="628"></td>

   <td width="2"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>




If you enter PETER  PAN  then

<table width="90%">

 <tbody>

  <tr>

   <td colspan="2"><strong>COST </strong></td>

  </tr>

  <tr>

   <td colspan="2">-1</td>

  </tr>

  <tr>

   <td colspan="2"></td>

  </tr>

  <tr>

   <td width="317"></td>

   <td width="316"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>




If you enter 07044 then

<table width="90%">

 <tbody>

  <tr>

   <td colspan="4"><strong>COST </strong></td>

  </tr>

  <tr>

   <td colspan="4">1195</td>

  </tr>

  <tr>

   <td colspan="4"></td>

  </tr>

  <tr>

   <td colspan="2"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

  <tr>

   <td width="3"></td>

   <td width="429"></td>

   <td width="199"></td>

   <td width="2"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>

If you enter 11209 then

<table width="90%">

 <tbody>

  <tr>

   <td colspan="3"><strong>COST </strong></td>

  </tr>

  <tr>

   <td colspan="3">7070</td>

  </tr>

  <tr>

   <td colspan="3"></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td width="3"></td>

   <td width="628"></td>

   <td width="2"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>




If you enter 11111  then

<table width="90%">

 <tbody>

  <tr>

   <td colspan="2"><strong>COST </strong></td>

  </tr>

  <tr>

   <td colspan="2">-1</td>

  </tr>

  <tr>

   <td colspan="2"></td>

  </tr>

  <tr>

   <td width="317"></td>

   <td width="316"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>





