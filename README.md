Download Link: https://assignmentchef.com/product/solved-cs532-homework3
<br>
<ol>

 <li>The following are some of the relations transformed from the ER diagram for the Student Registration System (note that some changes have been made due to the creation of a singleattribute key for Classes):</li>

</ol>

<strong>TAs(<u>B#</u>, level, pay_rate, office, office_hour_start_time, office_hour_end_time) Courses(<u>dept_code, course#</u>, title, credits, deptname) </strong>

<strong>Classes(<u>classid</u>, dept_code, course#, sect#, year, semester, start_time, end_time, limit, size, room, TA_B#) </strong>/* note: classid is added to serve as a single-attribute key */

<strong>Faculty(<u>B#</u>, first_name, last_name, rank, office, email, phone#, deptname) </strong>

<strong>            Enrollments(<u>Student_B#, classid, </u>lgrade, ngrade) </strong>

<strong>            </strong>

Do the following for each relation schema:

<ul>

 <li>Identify all non-trivial functional dependencies based on the Requirements Document (but take into consideration that classid is added as the primary key for Classes). For this question, we also make the following assumptions: (1) each dept_code corresponds to a unique department and vice versa; (2) only faculty members in the same department could share an office and a phone number. Don’t make other assumptions about the data. Use the union rule to combine the functional dependencies as much as possible to avoid having multiple functional dependencies with the same left-hand side but different right-hand side. Furthermore, if a functional dependency is redundant (i.e., it can be derived from the ones you keep), it should not be included.</li>

</ul>




<ul>

 <li> Use functional dependencies identified in Question 1(a) to determine whether or not the schema is in 3NF or in BCNF. Justify your conclusion. You need to compute all candidate keys for each relation first.</li>

</ul>




<ul>

 <li>For each schema that is not in 3NF, decompose it into 3NF schemas using Algorithm LLJD-DPD-3NF. Show the result after each step of the algorithm, i.e., show the candidate keys (from Question 1(b)), show the minimal cover (Step 2), show the decomposition based on functional dependencies in the minimal cover (Step 3), and mention whether an additional schema needs to be added to the decomposition (Step 4). Don’t forget to underscore the primary key of each new relation.</li>

</ul>

<ol start="2">

 <li>Consider the following table schema for accounts in a banking system:</li>

</ol>

1 Accounts(<u>acct#</u>, owner_id, owner_name, acct_type, balance, interest_rate, time_opened)

It has the following functional dependencies F = {acct# à own_id acct_type balance time_opened, owner_id à owner_name, acct_type balance à interest_rate}.

<ul>

 <li> Explain why the schema is not in BCNF.</li>

 <li> Use Algorithm LLJD-BCNF to decompose it. Show the steps.</li>

 <li> Is your decomposition dependency-preserving? Justify your answer.</li>

</ul>

<ol start="3">

 <li> Prove or disprove the following rules:</li>

</ol>

<ul>

 <li>{B à CD, AB à E, E à C} |= {AE à CD}</li>

 <li>{B à CD, AD à E} |= {AB à E}</li>

</ul>

When proving a rule, you can use all the six inference rules (i.e., reflexivity rule, augmentation rule, transitivity rule, decomposition rule, union rule and pseudotransitivity rule). To disprove a rule, construct a relation with appropriate attributes and tuples such that the tuples of the relation satisfy the functional dependencies on the left of the rule but do not satisfy the functional dependency on the right of the rule.


