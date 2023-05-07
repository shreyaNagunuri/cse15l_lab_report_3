# Lab Report 3

For the task of researching commands, I choose to spend my time examining the find command. The find command is useful because, as it is named, it helps the user find 
certain directories or files depending on search that is made. In this lab report, I will demonstrate four unique uses of the command find and will show examples for each case. 

1. -type
This addition to the find command is particularly useful when trying to find a specific file/directory/link or more since it can limit the search to those specific types. 
The following example will show why this is useful:

```
(base) MacBook-Air-8:docsearch shreyanagunuri$ find /Users/shreyanagunuri/docsearch -type d
/Users/shreyanagunuri/docsearch/technical
/Users/shreyanagunuri/docsearch/technical/government
/Users/shreyanagunuri/docsearch/technical/government/About_LSC
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen
/Users/shreyanagunuri/docsearch/technical/government/Alcohol_Problems
/Users/shreyanagunuri/docsearch/technical/government/Gen_Account_Office
/Users/shreyanagunuri/docsearch/technical/government/Post_Rate_Comm
/Users/shreyanagunuri/docsearch/technical/government/Media
/Users/shreyanagunuri/docsearch/technical/plos
/Users/shreyanagunuri/docsearch/technical/biomed
/Users/shreyanagunuri/docsearch/technical/911report
```
The original technical directory has many, many files and we are able to significantly limit it to the directories in this file by simply typing this command. 

Another example of a use find is when I ran find /Users/shreyanagunuri/docsearch -type f . As shown below, there are hundreds of files in the current working directory. 
This command can also be used to show what is not there, when I did type l, c, b, p, and s nothing showed up since none of those types were avalible in the directory. 
```
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -type l
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -type c
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -type b
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -type p
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -type s
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -type f
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/Progress_report.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/Strategic_report.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/Comments_on_semiannual.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/Special_report_to_congress.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/CONFIG_STANDARDS.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/commission_report.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/diversity_priorities.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/reporting_system.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/State_Planning_Report.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/Protocol_Regarding_Access.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/ODonnell_et_al_v_LSCdecision.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/conference_highlights.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/State_Planning_Special_Report.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/multi102902.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/section-by-section_summary.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/jeffordslieberm.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/final.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/ctf7-10.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/ctf1-6.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/ro_clear_skies_book.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/ctm4-10.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/1-3_meth_901.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/atx1-6.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/tech_sectiong.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/bill.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/nov1.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/tech_adden.txt
/Users/shreyanagunuri/docsearch/technical/government/Alcohol_Problems/Session2-PDF.txt
/Users/shreyanagunuri/docsearch/technical/government/Alcohol_Problems/Session3-PDF.txt
/Users/shreyanagunuri/docsearch/technical/government/Alcohol_Problems/DraftRecom-PDF.txt
/Users/shreyanagunuri/docsearch/technical/government/Alcohol_Problems/Session4-PDF.txt
/Users/shreyanagunuri/docsearch/technical/government/Gen_Account_Office/d0269g.txt

```
Link to Source : https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/
2. -size
This mode is able to filter the search results when find is run to only print things in the directory under a specific size. -size can be used along -type to produce
interesting results. 
Here is an example of how they can be used together:
```
(base) MacBook-Air-8:technical shreyanagunuri$ find . -type d -size -1M
.
./government
./government/About_LSC
./government/Env_Prot_Agen
./government/Alcohol_Problems
./government/Gen_Account_Office
./government/Post_Rate_Comm
./government/Media
./plos
./biomed
./911report
```
To explain this in more detail, we can see that find is used with a type of -d (directory) and looking for directories with a size of under 1MB. I found this command useful since
sometimes I need to delete larger files in my computer to save space. I can imagine this command being useful to look for small or large directories/files to delete.
Another of example of -size is a more general search without the type being applied and a different size. 
```
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -size -2k
/Users/shreyanagunuri/docsearch/technical
/Users/shreyanagunuri/docsearch/technical/government
/Users/shreyanagunuri/docsearch/technical/government/About_LSC
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen
/Users/shreyanagunuri/docsearch/technical/government/Alcohol_Problems
/Users/shreyanagunuri/docsearch/technical/government/Post_Rate_Comm
/Users/shreyanagunuri/docsearch/technical/government/Media/Helping_Hands.txt
/Users/shreyanagunuri/docsearch/technical/government/Media/Campaign_Pays.txt
/Users/shreyanagunuri/docsearch/technical/government/Media/Fire_Victims_Sue.txt
/Users/shreyanagunuri/docsearch/technical/government/Media/Court_Keeps_Judge_From.txt
/Users/shreyanagunuri/docsearch/technical/government/Media/It_Pays_to_Know.txt
/Users/shreyanagunuri/docsearch/technical/government/Media/Self-Help_Website.txt
/Users/shreyanagunuri/docsearch/technical/government/Media/Justice_requests.txt
/Users/shreyanagunuri/docsearch/technical/government/Media/Wilmington_lawyer.txt
/Users/shreyanagunuri/docsearch/technical/government/Media/Lawyer_Web_Survey.txt
/Users/shreyanagunuri/docsearch/technical/plos/pmed.0020048.txt
/Users/shreyanagunuri/docsearch/technical/plos/pmed.0020028.txt
/Users/shreyanagunuri/docsearch/technical/plos/pmed.0020191.txt
/Users/shreyanagunuri/docsearch/technical/plos/pmed.0020226.txt
/Users/shreyanagunuri/docsearch/technical/plos/pmed.0020192.txt
/Users/shreyanagunuri/docsearch/technical/plos/pmed.0020157.txt
/Users/shreyanagunuri/docsearch/technical/plos/pmed.0020082.txt
/Users/shreyanagunuri/docsearch/technical/plos/pmed.0020120.txt
/Users/shreyanagunuri/docsearch/technical/911report
```
In this particular find, we are looking at directories and files and examining those that are under 2 kilobytes. This search may be useful when trying to catch a wider
net in terms of finding whatever in particular.

Link to Source: https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/#find-files-by-size

3. -delete
As named, this mode to find will delete files under certain specification. To assist with this our examples, I will be using -empty command which will search for empty file/directories and more. 

The first example is shown below:
```
(base) MacBook-Air-8:technical shreyanagunuri$ mkdir Project1
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -empty -type d
/Users/shreyanagunuri/docsearch/technical/Project1
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -empty -type d -delete
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical/Project1
find: /Users/shreyanagunuri/docsearch/technical/Project1: No such file or directory
```
To explain this example in more detail, I firstly created a directory called Project1. Then, show (using find) that there exists a directory called Project1. 
Next, I use find /Users/shreyanagunuri/docsearch/technical -empty -type d -delete to delete the file. Finally, I search for Project1 and nothing comes up showing that it has been deleted. 
I find this useful because there are plenty of circumstances were empty directories can be made and unused, so this can declutter directories. 

Another example of this being used is looking a specific type of file and deleting it is shown below

```
(base) MacBook-Air-8:technical shreyanagunuri$ ls
911report	Project1.java	biomed		government	plos
(base) MacBook-Air-8:technical shreyanagunuri$ find . -type f -name "Project1.java" -delete
(base) MacBook-Air-8:~ shreyanagunuri$ cd docsearch/
(base) MacBook-Air-8:docsearch shreyanagunuri$ cd technical
(base) MacBook-Air-8:technical shreyanagunuri$ ls
911report	biomed		government	plos
```
In this example, I run find . -type f -name "Project1.java" -delete in order to delete a java file callde Project1. I found this command incredibly useful since it is a convinent way to delete
a specific file especially if you have the path. 

Link to Source: https://www.cyberciti.biz/faq/howto-find-delete-empty-directories-files-in-unix-linux/

4. -mtime
This mode for find is a way to filter the search results by when the directory/file was made. 

An example of this being used is shown in the code block below:

```
(base) MacBook-Air-8:technical shreyanagunuri$ mkdir lab_report
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -mtime -5 
/Users/shreyanagunuri/docsearch/technical
/Users/shreyanagunuri/docsearch/technical/government
/Users/shreyanagunuri/docsearch/technical/government/.DS_Store
/Users/shreyanagunuri/docsearch/technical/.DS_Store
/Users/shreyanagunuri/docsearch/technical/lab_report
```
We can clearly see that the directory that I just made, appeared in the list of the directories/files appeared in the list of those made in less than five days ago. I found this command
useful because sometimes we need to delete all recently made files and find it like this is very simple. 

Another example be shown with a open index for when things should be made. 

```
(base) MacBook-Air-8:technical shreyanagunuri$ find /Users/shreyanagunuri/docsearch/technical -mtime +3
/Users/shreyanagunuri/docsearch/technical/government/About_LSC
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/Progress_report.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/Strategic_report.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/Comments_on_semiannual.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/Special_report_to_congress.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/CONFIG_STANDARDS.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/commission_report.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/diversity_priorities.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/reporting_system.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/State_Planning_Report.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/Protocol_Regarding_Access.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/ODonnell_et_al_v_LSCdecision.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/conference_highlights.txt
/Users/shreyanagunuri/docsearch/technical/government/About_LSC/State_Planning_Special_Report.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/multi102902.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/section-by-section_summary.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/jeffordslieberm.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/final.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/ctf7-10.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/ctf1-6.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/ro_clear_skies_book.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/ctm4-10.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/1-3_meth_901.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/atx1-6.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/tech_sectiong.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/bill.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/nov1.txt
/Users/shreyanagunuri/docsearch/technical/government/Env_Prot_Agen/tech_adden.txt
/Users/shreyanagunuri/docsearch/technical/government/Alcohol_Problems
```
This example is unique because it shows what happens if you use a plus sign with a specific days number. It will show anything made more 3 agos. This open index will be useful 
in seeing what files can be deleted from a certain timepoint. 

Link to Source: https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/#find-files-by-modification-date




