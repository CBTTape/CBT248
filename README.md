# CBT248
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 248 IS FROM JIM BOYSEN OF AMDAHL FEDERAL SERVICE CORP.    *   FILE 248
//*           IN IOWA.  THIS FILE CONTAINS UTILITIES WHICH          *   FILE 248
//*           FIND MEMBERS OR PROCS IN LARGE CONCATENATIONS, ETC.   *   FILE 248
//*           ALL PROGRAMS OR COMMANDS ARE WRITTEN IN ASSEMBLER.    *   FILE 248
//*                                                                 *   FILE 248
//*         CONTACT:  JIM BOYSEN, SR. SYSTEMS ENGINEER              *   FILE 248
//*                   AMDAHL FEDERAL SERVICE CORPORATION            *   FILE 248
//*                   12020 SUNRISE VALLEY DRIVE                    *   FILE 248
//*                   SUITE 380                                     *   FILE 248
//*                   RESTON VA 22091                               *   FILE 248
//*                                                                 *   FILE 248
//*                   (309) 793-1369 OR (309) 782-8334              *   FILE 248
//*                                                                 *   FILE 248
//*           ALL COMMANDS AND PROGRAMS HAVE BEEN TESTED AT         *   FILE 248
//*           SP 5.2 AS THOROUGHLY AS POSSIBLE, BUT NOTHING IS      *   FILE 248
//*           GUARANTEED, THEY WILL PROVIDED EXCELLENT EXAMPLES     *   FILE 248
//*           OF HOW TO DO SOME OF THIS STUFF.                      *   FILE 248
//*                                                                 *   FILE 248
//*    CLEARBC       PROGRAM TO DELETE ALL MESSAGES FOR A GIVEN     *   FILE 248
//*                  USERID FROM SYS1.BRODCAST, TO STOP THE         *   FILE 248
//*                  BROADCAST DATASET FROM CLOGGING UP.            *   FILE 248
//*                  (FOR MORE PROGRAMS IN THIS AREA, SEE FILE      *   FILE 248
//*                  247 FROM JIM MARSHALL AND SAM GOLOB.)          *   FILE 248
//*                                                                 *   FILE 248
//*    CPUINFO       SOURCE CODE FOR DISPLAYING VARIOUS SYSTEM      *   FILE 248
//*                  CONTROL BLOCK INFO AT USERS TSO TERMINAL.      *   FILE 248
//*                  SEE CODE DOC FOR FURTHER DETAILS.              *   FILE 248
//*                                                                 *   FILE 248
//*    CPUINFO$      JCL TO ASSEMBLE/LINK CPUINFO                   *   FILE 248
//*                                                                 *   FILE 248
//*    CPUINFO#      HELP FOR CPUINFO COMMAND                       *   FILE 248
//*                                                                 *   FILE 248
//*    GTEDAALC      DYNAMIC ALLOCATION MACRO FROM CHUCK HOFFMAN    *   FILE 248
//*                  OF GTE LAB FROM CBT TAPE USED BY VARIOUS       *   FILE 248
//*                  PROGRAMS                                       *   FILE 248
//*                                                                 *   FILE 248
//*    GTEDADAT      DYNAMIC ALLOCATION MACRO FROM CHUCK HOFFMAN    *   FILE 248
//*                  OF GTE LAB FROM CBT TAPE USED BY VARIOUS       *   FILE 248
//*                  PROGRAMS                                       *   FILE 248
//*                                                                 *   FILE 248
//*    GTEDADOC      DOCUMENTATION FOR THE GTE DYNAMIC ALLOCATION   *   FILE 248
//*                  MACROS                                         *   FILE 248
//*                                                                 *   FILE 248
//*    GTEDASET      DYNAMIC ALLOCATION MACRO FROM CHUCK HOFFMAN    *   FILE 248
//*                  OF GTE LAB FROM CBT TAPE USED BY VARIOUS       *   FILE 248
//*                  PROGRAMS                                       *   FILE 248
//*                                                                 *   FILE 248
//*    IEFUTL        ALLOW TSO SESSIONS TO BE DISCONNECTED AND      *   FILE 248
//*                  THEN 622 CANCEL ONCE DISCONNECT LIMIT HAS      *   FILE 248
//*                  BEEN EXCEEDED.  EXTEND JOB TIME FOR 20         *   FILE 248
//*                  MINUTE INCREMENTS AND ISSUE MESSAGE TO         *   FILE 248
//*                  NOTIFY USER/OPERATOR OF THIS EXTENSION.        *   FILE 248
//*                  THE TSO DISCONNECT WORKS WITH MULTIPLE         *   FILE 248
//*                  SESSION MANAGERS BECAUSE IT DISCONNECTS THE    *   FILE 248
//*                  LU AND NOT THE TERMINAL ID WHICH CAN BE A      *   FILE 248
//*                  BAD THING UNDER A MULTIPLE SESSION MANAGER.    *   FILE 248
//*                                                                 *   FILE 248
//*    IEFUTL$       JCL TO ASSEMBLE/LINK IEFUTL                    *   FILE 248
//*                                                                 *   FILE 248
//*    LCICS         LIST DATASETS ALLOCATED TO CICS DDNAME         *   FILE 248
//*                  DFHRPL OR IF LOAD MODULE SPECIFIED, SEARCH     *   FILE 248
//*                  THROUGH THE DATASETS FOR THE LOAD MODULE AND   *   FILE 248
//*                  DISPLAY DATASET(S) WHERE FOUND.  CALLS         *   FILE 248
//*                  LCICSXM TO OBTAIN TIOT AND DSNS FROM           *   FILE 248
//*                  SECONDARY ADDRESS SPACE (CICS).  COMMAND       *   FILE 248
//*                  NAME MUST BE PUT IN IKJTSO00 AS AUTH CMD.      *   FILE 248
//*                                                                 *   FILE 248
//*    LCICS$        JCL TO ASSEMBLE/LINK LCICS                     *   FILE 248
//*                                                                 *   FILE 248
//*    LCICS#        HELP FOR LCICS                                 *   FILE 248
//*                                                                 *   FILE 248
//*    LCICSXM       SUB PROGRAM TO HANDLE CROSS MEMORY ACCESS      *   FILE 248
//*                  TO CICS ADDRESS SPACE.                         *   FILE 248
//*                                                                 *   FILE 248
//*    LCICSXM$      JCL TO ASSEMBLE/LINK LCICSXM                   *   FILE 248
//*                                                                 *   FILE 248
//*    LISTV         LIST VOLUME INFORMATION.  ORIGINAL CODE        *   FILE 248
//*                  FROM EARLIER CBT TAPE ? WITH MODIFICATIONS     *   FILE 248
//*                  TO SHOW DEVICE STATUS (STORAGE, PRIVATE,       *   FILE 248
//*                  PUBLIC) AND DEVICE TYPE                        *   FILE 248
//*                  (3380,3390-2,3390-3).                          *   FILE 248
//*                                                                 *   FILE 248
//*    LISTV$        JCL TO ASSEMBLE/LINK LISTV                     *   FILE 248
//*                                                                 *   FILE 248
//*    LISTV#        HELP MEMBER FOR LISTV                          *   FILE 248
//*                                                                 *   FILE 248
//*    LLIST         DISPLAY LINKLIST AND LPA DATASETS OF THE       *   FILE 248
//*                  ACTIVE SYSTEM, AND IF LOAD MODULE IS           *   FILE 248
//*                  SPECIFIED, SEARCH STEPLIB, LINKLIST AND LPA    *   FILE 248
//*                  FOR MODULE AND REPORT IF FOUND AND WHERE       *   FILE 248
//*                  FOUND.  LISTS ALL LIBRARIES WHERE MODULE IS    *   FILE 248
//*                  FOUND.                                         *   FILE 248
//*                                                                 *   FILE 248
//*    LLIST$        JCL TO ASSEMBLE/LINK LLIST                     *   FILE 248
//*                                                                 *   FILE 248
//*    LLIST#        HELP FOR LLIST                                 *   FILE 248
//*                                                                 *   FILE 248
//*    LOOKDD        SEARCH THROUGH SPECIFIED DDNAME FOR SPECIFIED  *   FILE 248
//*                  MEMBER.  REPORT IF FOUND, WHAT DSNS IN         *   FILE 248
//*                  CONCATENATION CONTAIN MEMBER.  VERY USEFUL     *   FILE 248
//*                  IN ISPF DEBUGGING AND DEVELOPMENT AS WELL AS   *   FILE 248
//*                  SEARCHING FOR CLISTS/REXX IN DEVELOPMENT AND   *   FILE 248
//*                  DEBUGGING.                                     *   FILE 248
//*                                                                 *   FILE 248
//*    LOOKDD$       JCL TO ASSEMBLE/LINK LOOKDD                    *   FILE 248
//*                                                                 *   FILE 248
//*    LOOKDD#       HELP FOR LOOKDD                                *   FILE 248
//*                                                                 *   FILE 248
//*    LPROC         LIST DATASETS ALLOCATED TO JES2 PROCLIB        *   FILE 248
//*                  CONCATENATIONS, OR IF SPECIFIED, SEARCH        *   FILE 248
//*                  THROUGH CONCATENATION FOR SPECIFIED MEMBER     *   FILE 248
//*                  AND REPORT DATASET(S) WHERE PROC IS FOUND.     *   FILE 248
//*                  COMMAND NAME MUST BE PUT IN IKJTSO00 AS        *   FILE 248
//*                  AUTH CMD.                                      *   FILE 248
//*                                                                 *   FILE 248
//*    LPROC$        JCL TO ASSEMBLE/LINK LPROC                     *   FILE 248
//*                                                                 *   FILE 248
//*    LPROC#        HELP FOR LPROC                                 *   FILE 248
//*                                                                 *   FILE 248
//*    LPROCXM       SUB PROGRAM TO HANDLE CROSS MEMORY ACCESS      *   FILE 248
//*                  TO JES2 ADDRESS SPACE.                         *   FILE 248
//*                                                                 *   FILE 248
//*    LPROCXM$      JCL TO ASSEMBLE/LINK LPROCXM                   *   FILE 248
//*                                                                 *   FILE 248
//*    MCSCMD        THIS PROGRAM WILL RUN AS A STARTED TASK AND    *   FILE 248
//*                  USES THE MVS MODIFY COMMAND TO COMMUNICATE     *   FILE 248
//*                  WITH THE TASK.  IT ENABLES OPERATORS TO        *   FILE 248
//*                  ENTER A SYSTEM COMMAND AS IF IT CAME FROM      *   FILE 248
//*                  THE MASTER CONSOLE, I.E.   CF COMMANDS FROM    *   FILE 248
//*                  A MCS CONSOLE ENTER   F MCSCMD,END  TO         *   FILE 248
//*                  TERMINATE THE TASK                             *   FILE 248
//*                                                                 *   FILE 248
//*    MCSCMD$       JCL TO ASSEMBLE/LINK MCSCMD                    *   FILE 248
//*                                                                 *   FILE 248
//*    MCSCMD#       PROC TO RUN MCSCMD                             *   FILE 248
//*                                                                 *   FILE 248
//*    MCSESA        MCS FOR ESA                                    *   FILE 248
//*                                                                 *   FILE 248
//*    SMFCPUID      SET TSO CLIST/REXX VARIABLE (&SMFCPUID)        *   FILE 248
//*                  TO VALUE OF SMF SYSTEM ID                      *   FILE 248
//*                                                                 *   FILE 248
//*    SMFCPU$       JCL TO ASSEMBLE/LINK SMFCPUID                  *   FILE 248
//*                                                                 *   FILE 248
//*    SMFCPU#       HELP FOR SMFCPUID                              *   FILE 248
//*                                                                 *   FILE 248
```
