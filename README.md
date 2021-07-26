# Convert DITA 1.3 maps and topics to the DITA 2.x standard

## Installation

To install the add-on, follow these instructions:

1. Go to **Help > Install new add-ons...** to open an add-on selection dialog box.
2. Enter or paste https://raw.githubusercontent.com/oxygenxml/dita_1_3_to_2_x_convert/main/addon.xml in the **Show add-ons from** field.
3. Select the **Convert DITA 1.3 maps and topics to the DITA 2.x standard** add-on and click **Next**.
4. Read the end-user license agreement. Then select the **I accept all terms of the end-user license agreement** option and click **Install**.
5. Restart the application.

**Result:** In the application main menu **Tools->XML Refactoring** dialog you will find a new refactoring action named "Convert DITA 1.3 maps and topics to the DITA 2.x standard" which can be applied on your DITA resources.

The refactoring action performs the following changes:
*   Changes DOCTYPE declarations and XML Schema/Relax NG schema references.
*   DITA Map changes:
    *   Removes the `@lockmeta` attribute.
    *   Removes the `<topicset>` and `<topicsetref>` elements.
    *   Migrates the `@navtitle` attribute as a `<navtitle>` element.
    *   Migrates the `@title` attribute as a `<title>` element.
    *   Converts the `@copy-to` attribute to a `<resourceid>` element.
    *   Replaces the `@print` attribute with an `@deliveryTarget` attribute.
    *   Convert topicmeta `<linktext>` to `<linktitle>`
*   DITA task changes:
    *   Converts the `<substep>` element to a `<step>` element.
    *   Converts the `<substeps>` element to a `<steps>` element.
*   DITA topic changes:
    *   Removes the `@type` attribute with the value `fastpath`.
    *   Converts the `@alt` attribute to an `<alt>` element.
    *   Replaces the `<index-sort-as>` element with a `<sort-as>` element.
    *   Removes the `<itemgroup>` element.
    *   Moves the contents of the `<titlealts>` element inside the `<prolog>`.
    *   Removes the `@domains` attribute.
    *   Renames `<sectiondiv>` to `<div>`.
    *   Remove `@query` attribute from `<link>` element.
