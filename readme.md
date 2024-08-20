# Guide to use Maestro #
### Tools and Software need it ###
* Android Studio
* Java
* Xcode
* Node.js

To install and use Maestro please follow the instructions in the next link.
https://maestro.mobile.dev/

### Basic Structure and Scripting ####
All the Test Scripts are .yaml files.

```
appId: your.app.id
---
- launchApp
- tapOn: "Text on the screen"

```
 
 On the **Resources** folder we are going to include the Resources that we are going to use for testing purposes, such as APKs, Apps, images, JSON files, etc.

 On the **Pages** folder we are going to include the POM pages for out test scripts. 

On the **Tests** folder we are going to create our .yaml test files.

 ### Locators ###
 In few words, a locator is a way to identify an element in the UI.

### POM ####
Page Objet Model is an automation dessing patten in which we create a file that contains all the UI elements (and sometimes functions or methos) that are going to be uses in a particular Page or Screen. So if there is a change in the UI for a specific Page or Screen in the application, we are going to update only that element locator in that specific Page or Screen file.

So, for example. The file name LoginPage only contains the UI elements of that scpecific Login Page in the application, using POM we avoid to duplicate code.

We are going to create our POM files in the Pages folder.

```
// ExamplePage.js
output.login = {
    txtEmail: 'email_text', 
    txtPassword: 'password_text',
    btnLogin: 'loginButton',
    btnRegister: 'registerButton'
}
```
### Naming Conventions for Locators ###
```
+----------+----------------------------+--------+-----------------+
| Category |      UI/Control type       | Prefix |     Example     |
+----------+----------------------------+--------+-----------------+
| Basic    | Button                     | btn    | btnExit         |
| Basic    | Check box                  | chk    | chkReadOnly     |
| Basic    | Combo box                  | cbo    | cboEnglish      |
| Basic    | Common dialog              | dlg    | dlgFileOpen     |
| Basic    | Date picker                | dtp    | dtpPublished    |
| Basic    | Dropdown List / Select tag | ddl    | ddlCountry      |
| Basic    | Form                       | frm    | frmEntry        |
| Basic    | Frame                      | fra    | fraLanguage     |
| Basic    | Image                      | img    | imgIcon         |
| Basic    | Label                      | lbl    | lblHelpMessage  |
| Basic    | Links/Anchor Tags          | lnk    | lnkForgotPwd    |
| Basic    | List box                   | lst    | lstPolicyCodes  |
| Basic    | Menu                       | mnu    | mnuFileOpen     |
| Basic    | Radio button / group       | rdo    | rdoGender       |
| Basic    | RichTextBox                | rtf    | rtfReport       |
| Basic    | Table                      | tbl    | tblCustomer     |
| Basic    | TabStrip                   | tab    | tabOptions      |
| Basic    | Text Area                  | txa    | txaDescription  |
| Basic    | Text box                   | txt    | txtLastName     |
| Complex  | Chevron                    | chv    | chvProtocol     |
| Complex  | Data grid                  | dgd    | dgdTitles       |
| Complex  | Data list                  | dbl    | dblPublisher    |
| Complex  | Directory list box         | dir    | dirSource       |
| Complex  | Drive list box             | drv    | drvTarget       |
| Complex  | File list box              | fil    | filSource       |
| Complex  | Panel/Fieldset             | pnl    | pnlGroup        |
| Complex  | ProgressBar                | prg    | prgLoadFile     |
| Complex  | Slider                     | sld    | sldScale        |
| Complex  | Spinner                    | spn    | spnPages        |
| Complex  | StatusBar                  | sta    | staDateTime     |
| Complex  | Timer                      | tmr    | tmrAlarm        |
| Complex  | Toolbar                    | tlb    | tlbActions      |
| Complex  | TreeView                   | tre    | treOrganization |
+----------+----------------------------+--------+-----------------+
```
