Author:
=======
Rolf Laudenbach (rlaudenbach@aras.com) - see installation steps below -

Version:
========
v2-1 (August 2013)
 - Added i18n support for toolbar, menus and messages. (language files in: Client/Solutions/DocumentHieratchies/xml)
 - Added language_effectivity on "Document Section Document" relationship. Defaults to "ALL" but can be maintained for specific language issues of documents.
   When Hierarchy is viewed from TOC the current user's language code will be used to filter by language effectivity.

v2-0 (August 2013)
- Grid actions to:
   - add Sub sections
   - Lock/Unlock
   - add existing documents from grid

- added a grid column to highlight when document of released 'Sections' have newer generations (not is_current)

- 2 effectivity views on grid to show "current versions of Rev" and "Released versions of Rev"  (Rev = Revisions of Document Sections)

- Changed auto number prefix to DBK-XXXX

- Changed TOC variable naming convention (that point to 'Book' connected to TOC-items). Naming = TOCDBK_<Item Type Name>

- logic on TOC Variable can read item_number and item_number,major_rev of an identified 'Book'. The released version
  within the defined major_rev is pulled when viewing from TOC directly. If major_rev is missing, the latest released Rev is pulled.

- added more checking for gird actions. like Is owner of row item ? or is owner/manager at root item (Book or Top Section) ?

- Improved grid loading and loading status messages.

- loads on top of older versions v1-3 / v1-4 but many ItemType, Realshionship, Action, Methods have updated naming.
  (i.e. 'Document Collection' is now 'Document Book'. Hierarchy Nodes are now 'Document Sections'


Description (Document Hierarchies)
==================================

- Adds new Item Types to build Document Hierarchy Structures linking to individual documents

- Much like Bills Of Materials, Document Hierarchies are versionable and operate on a 
  life cycle (Preliminary->Released->Obsolete)

- A separate ItemType „Document Book“, also versionable, is used to group „Document Sections“ hierarchically
  Each "Document Section" can have owners and co-owners for exteded access control.
  Life cycles drive "Book" and "Sections" from 'Prliminary' to 'Released' to 'Obsolete'

- „Dummy“ TOC Item Types can be used to set up a direct access to a 'Document Book' from the TOC.
   Such as a „Quality Handbook“ or an „Operations Manual“ or more. TOC-Access on these items define who have access to 
   these "Books" from the TOC directly. If displayed from TOC the effectivity is fixed to "Released 
   This package includes the example for a „Quality Handbook“

- Owners and Co-Owners are allowed to do "Manual Release" of the structure (down) for „Document Books“ 
  and on every level of „Document Sections“.

- Manual Revisioning  is also allowed for Owners. If revisioning is started on a node within the document hierarchy,
  then all  nodes on the path to the top (including to „Document Book“) will be automatically revisioned, as well. (up)

- Linked Documents must still follow their own release and revisioning process.

- Hierarchy nodes linking to documents will  show  released  documents only , if the effectivity view 
  on the grid is set to „Released versions of Rev“.  Else the current version of linked documents will be shown.

- If a newer released version of a linked document is available on a "Released" Document Section, an icon on the grid will indicate this.
  In this case the "Owner" of the "Document Section" can run an action to pull in this latest released document.


Package Installation Steps
==========================
... Use the Aras import utiltity tool and log on to the target Aras System and Database with "admin"


--------------------------------------------
Stage - 0 Import subset of "Common Utilities"  (as admin)


Select Mainfest file from folder .\0-Common Utilties v1-8 (partial)\imports.mf and set option "Merge"

then, click the "import" button on top tool bar


--------------------------------------------
Stage - 1  Import Core Extensions  (as root)


Select Mainfest file from folder .\1-Innovator Core Extensions\imports (root).mf and set option "Merge"

then, click the "import" button on top tool bar


--------------------------------------------
Stage - 2  Import the Document Hierarchy Solution (as admin)

Select Mainfest file from folder .\2-Document Hierarchy Solution\imports (admin).mf and set option "Merge"

then, click the "import" button on top tool bar

(optional) - Import PackageVersion

    Select Mainfest file from folder .\2-Document Hierarchy Solution\imports (admin) - SetPackageVersion (Optional).mf and set option "Merge"

    then, click the "import" button on top tool bar - this requires "Package Utiltities" to be present. Else it will fail !!!



--------------------------------------------
Stage - 3  Updates Flags on existing Document Section Items 

--> Nash updates
--> you only need this if a previous version of Document Hierarchies is in use and there are existing folder structres in your DB

start Nash.aspx tool on the target Aras System and log on as "admin"
(the url to nash.aspy tool could be like this: http://localhost/InnovatorServer/Client/scripts/nash.aspx )

- use text editor and open file 
      .\3-nash update\UpdateFlagsOnExistigDocumentSectionItems.xml

  Select all and paste to Nash input box "XML"

  then, click submit button


(Optonal) - Merge a Variable

- use text editor and open file 
      .\3-nash update\Merge Variable - File Ext to View single File.xml

  Select all and paste to Nash input box "XML"

  then, click submit button



  done. Close the Nash tool


------------------------------------------------------------------------------------------------------
Stage - 4 Copy code tree overlay files to the code tree of the the target Aras System

- open folder "_CodeTreeOverlays" and select "innovator" and copy this folder
- on the target Aras System go to the installation folders and paste the copy over the "innovator" folder
- confirm to add or overwrite folders and files.



Dependencies
============
Common Utitlites
Package Utilities (optional)


available as Community Project
------------------------------
Yes


available separetely on Partner Portal
--------------------------------------
No


Version History:
================
v1-3 (September 2012)

v1-1 & v1-2  - Initial Prototypes


Notice of Liability
-------------------
The information contained in this document and the import packages are distributed on an "As Is" basis, 
without warranty of any kind, express or implied, including, but not limited to, the implied warranties 
of merchantability and fitness for a particular purpose or a warranty of non-infringement. Aras shall have 
no liability to any person or entity with respect to any loss or damage caused or alleged to be caused 
directly or indirectly by the information contained in this document or by the software or hardware products 
described herein.

