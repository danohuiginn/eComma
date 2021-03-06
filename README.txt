MODULE DEPENDENCIES

- comment
- comment_delete
- community_tags
- content
- jquery_update
- jquery_ui
- libraries
- page_manager
- panels
- tagadelic
- taxonomy
- text
- views
- views_bonus_export


INSTALLATION OF ECOMMA MODULE
 
Instructions below are based on navigation in admin menu (admin_menu module).

1.  Site building > Modules: enable ecomma module and dependencies
2.  As Described in the jquery_ui module: 
	-Download the latest jQuery UI 1.7 release from:
     http://code.google.com/p/jquery-ui/downloads/list?q=1.7
     
	-Put the downloaded archive into the directory:
     /sites/all/libraries/jquery.ui-1.7.zip
     
	-Extract the archive.  This will create the following sub-directory:
     /sites/all/libraries/jquery.ui-1.7/
     
	-Rename the sub-directory into "jquery.ui":
     /sites/all/libraries/jquery.ui/

(Go to content management > Content types for step 2-4)
3.  Add content type: Add custom content type.
4.  Edit new content type > Comment settings > Preview comment:Optional
5.  Edit new content type > Comment settings > Display below post or comments
6.  Manage fields > Add a new text area field with unlimited values
7.  Enable ecomma commentary features for that text area field in the settings.
8.  Taxonomy: Add Vocabulary and enable it for the new content type.
9.  Taxonomy: Check Settings > Tags checkbox
10.  Site Configurations > Community tags: Enable new vocabulary
11.  New content type  > Workflow settings > Community tagging form:Select Block
(Go to content User Management > Permissions for step 10-13)
12. Community_tags: Enable "tag content" for authenticated and anonymous users.
    (Enables unauthenticated users to see the tags, but not to tag.)
13. Community_tags: Enable "edit own tags" for authenticated.
14. Comment: Enable "access comments" for authenticated and anonymous users. 
    (Enables unauthenticated users to see the comments, but not to comment.)
15. Comment_delete: Enable "delete own comments" for authenticated  users.
16. Site building > Pages > List:
	-Enable node_view and click on edit. 
	-Selection rules > select "Node:type" and then check new content type
	-Left column: Add content > Node > Field: your-text-field
17. Create a node with new content type. 
18. Enter your text in the eComma enabled text field.

Current restrictions:
	* Does currently not work on IE browser.
	* Once a group/class has started to tag or comment on a text the text 
	  cannot be changed in any way or the annotations will be off.


*****************************************************************************

USE OF ECOMMA MODULE (see also screenshots at admin/help/ecomma)

1. Tags and Comments
		
	-A "tag" is a label that you can use to mark a word or series of words that
	 interest you.
	-A "comment" is a remark on passage of a text.
	-A user might mark an instance of metaphor with the tag "metaphor" or tag a
	 famous passage with "well-known"
	-You may use tags that previous readers have created or create your own.
	-Tags are arranged in a "tag cloud". The tags in the cloud are arranged
	 alphabetically, and tags that are used more frequently will appear larger.
	
2. Adding tags and comments to an eComma text

	Simply use your mouse to select a range of text in the text provided.
	This will cause a draggable dialog box to appear. You can select either
	to create a tag or a comment with the selected text.
	You can type one of more words into the tag creation box to add them to
	your selected text, or you can type a longer observation or question into
	the comment creation box. You can also reply to another user's comment
	by clicking the link that will appear under the comment if you are logged
	in. And you can edit and delete your already submitted comments.
	Tags can be deleted, but not edited.


3. The eComma interface

	-Use the centered icon tabs to navigate between the text's word cloud,
	 tag view, comment view, comment word cloud, and user annotation list.
	-Clicking a tag in the tag cloud shows all phrases in the text that have
	 been given this tag, as well as which users have added the tag, and when.
	-Clicking on the highlight button in the comment view will show all phrases
	 in the text that relate to that comment.
	-Clicking on the user name in the user annotation list to a list of all the
	 user's comments and tags for the current text.
		
	
4. Download eComma comments
			
		-Download  eComma comments data as XML or import to Google docs
		 spreadsheet. To download an XML file of the comment data, simply
		 click download comments button at the top of the comment view panel.
		-If you need to export the data to a spreadsheet format you can import
		 (stream) the xml directly and without downloading to a google spreadsheet. 
				*You will need a google account to work with this method.
				*You also need the text identification number of your ecomma text.
				 You can obtain the text id from the URL. It is the number that
				 follows /ecomma/node/.
				*Open a google spreadsheet and paste the following code into
				 the first cell:
		
        =importXML("http://www.coerll.utexas.edu/ecomma/ecomma_comments_export/
        [replace this (including brackets) with text-id]","//node")
	
	
5. Other drupal modules to consider

	-For collaborative class or group assignments try using the organic groups
	 module in combination with the userplus module.
	-This module provides some views in ecomma.views.inc.inc that may be used
	 with the module.
