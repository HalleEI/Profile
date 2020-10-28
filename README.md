# Profile

Country Club Analysis

•	Project Requirements
Working on a new country club with few different facilities that are offered. The club requires a monitor and understanding of how they can use their club’s data to analyze the higher demands they are getting, and which facilities are mostly in use by both their members and non-members.

•	Benefits
The benefit of this analysis is related with the requirement in that it helps the club focus more on the facilities that are mostly being utilized. As quality is more profitable than quantity, this analysis helps to pinpoint which facilities are being utilized more and increase the maintenance on those specific facilities than to spend more money in having and unused facility.

•	Tables Used
 
I have used 3 tables. Facilities, members, and bookings in each database.
-	 Facilities: 
    facid  = PRIMARY KEY
    name (of the facility)
    membercost 
    guestcost 
    initialoutlay (the cost of the initial construction/maintenance of the facility)
    monthlymaintenance 
-	Members :
    memid = PRIMARY KEY
    surname 
    firstname 
    address 
    zipcode 
    telephone 
    recommendedby (how many recommendations they had received to join)
    joindate 
    	FOREIGN KEY (recommendedby) REFERENCES members(memid) 

-	Bookings: 
    bookid  = PRIMARY KEY
    facid
    memid 
    starttime 
    slots
	FOREIGN KEY (facid) REFERENCES facilities(facid)
	FOREIGN KEY (memid) REFERENCES members(memid)

•	Technical Specifications

	Used Oracle VM and GCP to set up a Hadoop ecosystem with SQOOP, HIVE, and HBASE in an ubuntu environment.
	Used three database sources each created from 3 RDBMS’s. 
	Created a connection to MySQL server with MySQL workbench and setup one of my databases.
	Created a connection to PostgreSQL and MSSQL with Dbeaver and setup two of my databases.
	Used SQOOP data integration tool, to ingest my data from RDBMS to HDFS using the jdbc connectors for each RDBMS’s.
	On top of the 3 RDBMS sources I have a csv file source. 
	Used an SFTP (Secure File Transfer Protocol) to load/transfer CSV files from a non-RDBMS source into HDFS.
	Each databases have 3 tables.
	Created database that holds the RAW layer external tables in HIVE.
	Created database that holds the DSL internal tables in HIVE.
	Integrated HIVE tables with HBASE.
	Ran a scripting to run my Hadoop ecosystem from creation of Sqoop jobscreating Raw and DSL tableshive HBase integration tables.
	Used PySpark to ingest RDBMS data into my Hadoop Ecosystem.



