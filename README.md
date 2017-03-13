>## Archived Aras Community Project
*This project has been migrated to GitHub from the old Aras Projects page (http://www.aras.com/projects). As an Archived project, this project is no longer being actively developed or maintained.*

>*For current projects, please visit the new Aras Community Projects page on the updated Aras Community site: http://community.aras.com/projects*

# Document Hierarchies Management

New version 3-0 for Aras10. Please Continue to use v2-1 for Aras 9.x. Adds new Item Types to build Document Hierarchy Structures linking to individual documents.

Much like Bills Of Materials, Document Hierarchies must be versionable and operate on a life cycle (Preliminary->Released->Obsolete)

Manual release of the full structures is allowed for Owners and manual revisioning is also allowed for Owners.

If revisioning is started on a node within the document hierarchy, then all child nodes on the path (up) to the top get revisioned, automatically.

Linked documents must still follow their own release and revisioning process.

Releasing a document section will 'freeze' the link to the current version of related documents.

Read the concepts document and users guide to learn more

SOLUTION IS NOT COMPATIBLE WITH ARAS INNOVATOR 11.0

## History

Release notes/descriptions for the original project posted on the previous Aras Projects page.

Release | Notes
--------|--------
[v2.1](https://github.com/ArasLabs/doc-hierarchy-management/releases/tag/v2.1) | Improved grid loading and access controls. Document Collection is called Document Book now. Inernationalized (xml files) for toolbar. menus, messages on Folder Navigator. Download add-on import package and documentation. (imports on top of standard Aras Solutions).
[v1.3](https://github.com/ArasLabs/doc-hierarchy-management/releases/tag/v1.3) | add-on import package and conceptual overview document. (imports on top of standard Aras Solutions)

#### Supported Aras Versions

Project | Aras
--------|------
[v2.1](https://github.com/ArasLabs/doc-hierarchy-management/releases/tag/v2.1) | Aras 9.4
[v1.3](https://github.com/ArasLabs/doc-hierarchy-management/releases/tag/v1.3) | Aras 9.3

> ###### *Please note: Aras Community Projects are provided on an "as-is" basis.*

>*Due to the wide array of possible business requirements, customizations, and use cases, we cannot guarantee compatibility or support for any given project.*

>*If you experience issues with this or any other Aras Community Project, please contact the project author and file an issue on the project's GitHub repository. You can also check out the [Aras Developer Forums](http://community.aras.com/forums/) to see if any other community members have experienced the same issue.*

## Credits

**Project Owner:** Rolf Laudenbach, Aras Corporation

**Created On:** May 10, 2012

## License

This project is published under the Microsoft Public License license (MS-PL). See the [LICENSE file](./LICENSE.md) for license rights and limitations.
