Author:
-------
Rolf Laudenbach (rlaudenbach@aras.com)

Version:
--------
v1-3  (September 2012)


Description (Document Hierarchies)
------------
- Adds new Item Types to build Document Hierarchy Structures linking to individual documents

- Much like Bills Of Materials, Document Hierarchies are versionable and operate on a 
  life cycle (Preliminary->Released->Obsolete)

- A separate ItemType „Document Collection“, also versionable, is used to group a „Document Hierarchy“
  and allow different access control. Also operating on the same life cycle.

- „Dummy“ TOC Item Types can be used to set up a direct access to a document  hierarchy of a defined type,
   such as a „Quality Handbook“ or an „Operations Manual“ or more.
   This package includes the example for a „Quality Handbook“

- Owners and Co-Owners can be defined for „Document Collections“ and  every level of the „Document Hierarchy“.
  Manual Release of the full structure  (down) is allowed for Owners.

- Manual Revisioning  is also allowed for Owners. If revisioning is started on a node within the document hierarchy, then all  nodes on the path to the top (including to „Document Collection“) will be automatically revisioned, as well. (up)

- Linked Documents must still follow their own release and revisioning process.

- Hierarchy nodes linking to documents will  show  released  documents only , if the „query option“ 
  on the grid is set to „latest Released“.  Else the current version of linked documents will be shown.


Dependencies
------------
Common Utitlites


available as Community Project
------------------------------
Yes


available separetely on Partner Portal
--------------------------------------
No


Version History:
----------------
v1-1 & v1-2  - Initial Prototypes


Notice of Liability
-------------------
The information contained in this document and the import packages are distributed on an "As Is" basis, 
without warranty of any kind, express or implied, including, but not limited to, the implied warranties 
of merchantability and fitness for a particular purpose or a warranty of non-infringement. Aras shall have 
no liability to any person or entity with respect to any loss or damage caused or alleged to be caused 
directly or indirectly by the information contained in this document or by the software or hardware products 
described herein.

