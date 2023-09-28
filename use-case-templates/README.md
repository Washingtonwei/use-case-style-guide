# Scaffolding a Use Case with a Use Case Templates Repository

Besides the practical use case writing style guide introduced in [here](../README.md), we also developed a use case templates repository, where commonly used use cases are archived for reuse in different domain contexts. These use case templates are not meant to constrain the way a use case is written but to provide a starting point for requirements engineers. Think of them as intermediate good or semi-finished products, which need to be completed by requirements engineers to obtain a full-fledged use case specification.

An easy-to-copy-and-paste version of this repository is available at [Google Docs](https://docs.google.com/document/d/1mdpekQ3sbKstbhFWDMD8-wzQuPRi-Y46t9z1XhcQ2BI/edit?usp=sharing). A real project's use case specification following the style guide and using the templates repository is available at [here](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit?usp=sharing). Feel free to provide feedback.

> **Note**: A *&lt;whatever&gt;* as postulated by Alistair Cockburn represents an important business object. A requirements engineer only needs to substitute a concrete business object for *&lt;whatever&gt;*. Text enclosed in square brackets ''[]" and displayed in italics is included to provide guidance to the author and should be deleted before publishing the use case.

## Table of contents

1. [Find *&lt;whatever&gt;* s](#find-whatevers)
2. [View a *&lt;whatever&gt;*](#view-a-whatever)
3. [Create a *&lt;whatever&gt;*](#create-a-whatever)
4. [Change a *&lt;whatever&gt;*](#change-a-whatever)
5. [Delete a *&lt;whatever&gt;*](#delete-a-whatever)
6. [Generate a *&lt;report type&gt;* report](#generate-a-report)

<a name="find-whatevers"></a>

## 1. Find *&lt;whatever&gt;* s

<table style="text-align: right">
      <tr>
        <td>UC ID and Name:</td>
        <td style="width: 90%; text-align: left" colspan="3">
          UC-01: Find <em>&lt;whatever&gt;</em>s
        </td>
      </tr>
      <tr>
        <td>Created By:</td>
        <td style="width: 30%; text-align: left"></td>
        <td>Date Created:</td>
        <td style="width: 30%; text-align: left"></td>
      </tr>
      <tr>
        <td>Primary Actor:</td>
        <td style="width: 30%; text-align: left">User</td>
        <td>Secondary Actors:</td>
        <td style="width: 30%; text-align: left"></td>
      </tr>
      <tr>
        <td>Trigger:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          The User indicates to find <em>&lt;whatever&gt;</em>s.
        </td>
      </tr>
      <tr>
        <td>Description:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          The User wants to find <em>&lt;whatever&gt;</em>s which match specific
          criteria, so that she can decide what to do next or other
          <em>&lt;rationale of this use case&gt;</em>.
        </td>
      </tr>
      <tr>
        <td>Preconditions:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          PRE-1. The User is logged into the System.
        </td>
      </tr>
      <tr>
        <td>Postconditions:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          POST-1. A list of matching <em>&lt;whatever&gt;</em>s is returned and
          displayed to the User. It is possible that the list is empty.
        </td>
      </tr>
      <tr>
        <td>Main Success Scenario:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          <ol>
            <li>The User indicates to find <em>&lt;whatever&gt;</em>s.</li>
            <li>
              The System asks the User to enter search values according to
              the "Search criteria" defined in the Associated Information of this use
              case.
            </li>
            <li>
              The User enters one or more search values and confirms that she has
              finished entering.
            </li>
            <li>
              The System finds all <em>&lt;whatever&gt;</em>s that match the
              provided search criteria values.
            </li>
            <li>
              The System displays the matching <em>&lt;whatever&gt;</em>s according
              to the "Search results display strategy" and the "Sort criteria"
              defined in the Associated Information of this use case.
            </li>
            <li>Use case ends.</li>
          </ol>
        </td>
      </tr>
      <tr>
        <td>Extensions:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          <b>4a. No matching <em>&lt;whatever&gt;</em>s are found:</b> <br />
          4a1. The System alerts the User that no matching
          <em>&lt;whatever&gt;</em>s are found. <br />
          4a2. The User either chooses to <ins>UC-03: create a
            <em>&lt;whatever&gt;</em></ins> or chooses to terminate the use case or chooses to return to step
          2 of the normal flow. <br />
          <b
            >5a. The User chooses to select a different set of properties to
            display the matching <em>&lt;whatever&gt;</em>s:</b
          >
          <br />
          5a1. The System displays the current "Search results display
          strategy." <br />
          5a2. The User enters a customized "Search results display strategy,"
          confirms that she has finished entering, and returns to step 5 of the normal flow. <br />
          <b>5b. The User chooses to re-sort the search results: </b> <br />
          5b1. The User re-sorts the search result according to the "Sort criteria"
          defined in the Associated Information of this use case and returns to step
          5 of the normal flow.
        </td>
      </tr>
      <tr>
        <td>Priority:</td>
        <td style="width: 80%; text-align: left" colspan="3">High</td>
      </tr>
      <tr>
        <td>Frequency of Use:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          Approximately *** user, average of *** usages per week.
        </td>
      </tr>
      <tr>
        <td>Business Rules:</td>
        <td style="width: 80%; text-align: left" colspan="3"></td>
      </tr>
      <tr>
        <td>Associated Information:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          Search criteria (aka search fields, search attributes/properties,
          search details, searchable qualities):
          <table style="width: 100%">
            <tr>
              <th>Search property name</th>
              <th>Data type</th>
              <th>Validation rule</th>
              <th>Security/access concerns</th>
              <th>Reference to glossary</th>
            </tr>
            <tr>
              <td>First name</td>
              <td>String</td>
              <td>Required</td>
              <td></td>
              <td></td>
            </tr>
            <tr>
              <td>Last name</td>
              <td>String</td>
              <td>Required</td>
              <td></td>
              <td></td>
            </tr>
            <tr>
              <td>Phone number</td>
              <td>String</td>
              <td>Required, (999) 999-9999 format</td>
              <td></td>
              <td></td>
            </tr>
            <tr>
              <td>Physical address</td>
              <td>String</td>
              <td>
                Required, valid US address format (street, suite/room/floor,
                city, state, postal code)
              </td>
              <td></td>
              <td></td>
            </tr>
            <tr>
              <td>Email</td>
              <td>String</td>
              <td>Required, valid email</td>
              <td></td>
              <td></td>
            </tr>
          </table>
          Search results display strategy (specify which properties to display
          for each matching <em>&lt;whatever&gt;</em>):
          <ul>
            <li>TBD</li>
          </ul>
          Sort criteria:
          <ul>
            <li>TBD</li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>Related Use Cases:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          The User can perform other actions after this use case. After this use
          case succeeds, the User may select any of the displayed
          <em>&lt;whatever&gt;</em>s and take any of the following actions on
          the selected item:
          <ul>
            <li>UC-02: View a <em>&lt;whatever&gt;</em></li>
            <li>UC-03: Create a <em>&lt;whatever&gt;</em></li>
            <li>UC-04: Change a <em>&lt;whatever&gt;</em></li>
            <li>UC-05: Delete a <em>&lt;whatever&gt;</em></li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>Assumptions:</td>
        <td style="width: 80%; text-align: left" colspan="3"></td>
      </tr>
      <tr>
        <td>Open Issues:</td>
        <td style="width: 80%; text-align: left" colspan="3"></td>
      </tr>
    </table>

See examples that adopt this template: [Use Case 6: Spirit Director/SuperFrog Student finds appearance requests](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.lg725m8k6v7b) and [Use Case 15: Spirit Director finds SuperFrog Students](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.ifmhdqaelx3n).

**[⬆ back to top](#table-of-contents)**

<a name="view-a-whatever"></a>
## 2. View a *&lt;whatever&gt;*

<table style="text-align: right">
      <tr>
        <td>UC ID and Name:</td>
        <td style="width: 90%; text-align: left" colspan="3">
          UC-02: View a <em>&lt;whatever&gt;</em>
        </td>
      </tr>
      <tr>
        <td>Created By:</td>
        <td style="width: 30%; text-align: left"></td>
        <td>Date Created:</td>
        <td style="width: 30%; text-align: left"></td>
      </tr>
      <tr>
        <td>Primary Actor:</td>
        <td style="width: 30%; text-align: left">User</td>
        <td>Secondary Actors:</td>
        <td style="width: 30%; text-align: left"></td>
      </tr>
      <tr>
        <td>Trigger:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          The User indicates to view the details of a <em>&lt;whatever&gt;</em>.
        </td>
      </tr>
      <tr>
        <td>Description:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          The User wants to view the details of a <em>&lt;whatever&gt;</em>, so
          that she can get a better idea of <em>&lt;whatever&gt;</em> or other
          <em>&lt;rationale of this use case&gt;</em>.
        </td>
      </tr>
      <tr>
        <td>Preconditions:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          PRE-1. The User is logged into the System. <br />
          PRE-2. The User has the "view" privilege. See the Business Rules of this
          use case.
        </td>
      </tr>
      <tr>
        <td>Postconditions:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          POST-1. The details of the specified <em>&lt;whatever&gt;</em> are
          displayed to the User.
        </td>
      </tr>
      <tr>
        <td>Main Success Scenario:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          <ol>
            <li>
              The User indicates to view the details of a
              <em>&lt;whatever&gt;</em>.
            </li>
            <li>
              The User finds a list of <em>&lt;whatever&gt;</em>s through <u>UC-01:
                Find <em>&lt;whatever&gt;</em>s</u>.
            </li>
            <li>
              The User views the list and chooses to view the details of one
              specific <em>&lt;whatever&gt;</em>.
            </li>
            <li>
              The System retrieves and displays the details of this
              <em>&lt;whatever&gt;</em> according to the "Details" defined in
              the Associated Information and the "Security/access concerns" defined in
              the Business Rules of this use case.
            </li>
            <li>
              The User views the details of this <em>&lt;whatever&gt;</em>.
            </li>
            <li>Use case ends.</li>
          </ol>
        </td>
      </tr>
      <tr>
        <td>Extensions:</td>
        <td style="width: 80%; text-align: left" colspan="3"></td>
      </tr>
      <tr>
        <td>Priority:</td>
        <td style="width: 80%; text-align: left" colspan="3">High</td>
      </tr>
      <tr>
        <td>Frequency of Use:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          Approximately *** user, average of *** usages per week.
        </td>
      </tr>
      <tr>
        <td>Business Rules:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          Security/access concerns
          <ul>
            <li>TBD</li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>Associated Information:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          <table style="width: 100%">
            <tr>
              <th>Property name</th>
              <th>Data type</th>
              <th>Editability</th>
              <th>Security/access concerns</th>
              <th>Reference to glossary</th>
            </tr>
            <tr>
              <td></td>
              <td></td>
              <td></td>
              <td></td>
              <td></td>
            </tr>
             <tr>
              <td></td>
              <td></td>
              <td></td>
              <td></td>
              <td></td>
            </tr>
          </table>
        </td>
      </tr>
      <tr>
        <td>Related Use Cases:</td>
        <td style="width: 80%; text-align: left" colspan="3">
          UC-01: Find <em>&lt;whatever&gt;</em>s <br/>
          The User can perform other actions after this use case. After this use case succeeds, the User may 		   take any of the following actions on this <em>&lt;whatever&gt;</em>:
          <ul>
            <li>UC-04: Change a <em>&lt;whatever&gt;</em></li>
            <li>UC-05: Delete a <em>&lt;whatever&gt;</em></li>
            <li>UC-: View a <em>&lt;whatever2&gt;</em></li>
            <li>UC-: View a <em>&lt;whatever3&gt;</em></li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>Assumptions:</td>
        <td style="width: 80%; text-align: left" colspan="3"></td>
      </tr>
      <tr>
        <td>Open Issues:</td>
        <td style="width: 80%; text-align: left" colspan="3"></td>
      </tr>
</table>

See examples that adopt this template: [Use Case 7: Spirit Director/SuperFrog Student views an appearance request](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.dsnj8yei2233) and [Use Case 16: Spirit Director views a SuperFrog Student account](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.19z0lulk43dd).

**[⬆ back to top](#table-of-contents)**

<a name="create-a-whatever"></a>

## 3. Create a *&lt;whatever&gt;*

<table style="text-align: right">
  <tr>
    <td>UC ID and Name:</td>
    <td style="width: 90%; text-align: left" colspan="3">
      UC-03: Create a <em>&lt;whatever&gt;</em>
    </td>
  </tr>
  <tr>
    <td>Created By:</td>
    <td style="width: 30%; text-align: left"></td>
    <td>Date Created:</td>
    <td style="width: 30%; text-align: left"></td>
  </tr>
  <tr>
    <td>Primary Actor:</td>
    <td style="width: 30%; text-align: left">User</td>
    <td>Secondary Actors:</td>
    <td style="width: 30%; text-align: left"></td>
  </tr>
  <tr>
    <td>Trigger:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      The User indicates to create a new <em>&lt;whatever&gt;</em>.
    </td>
  </tr>
  <tr>
    <td>Description:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      The User wants to create a new <em>&lt;whatever&gt;</em>, so that
      <em>&lt;rationale of this use case&gt;</em>.
    </td>
  </tr>
  <tr>
    <td>Preconditions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      PRE-1. The User is logged into the System. <br />
      PRE-2. The User has the "create" privilege. See the Business Rules of this
      use case. <br />
      PRE-3. If this <em>&lt;whatever&gt;</em> is a dependent object, in
      other words, cannot exist by itself, the dependency object must exist
      first.
    </td>
  </tr>
  <tr>
    <td>Postconditions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      POST-1. The new <em>&lt;whatever&gt;</em> is stored in the System.
    </td>
  </tr>
  <tr>
    <td>Main Success Scenario:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      <ol>
        <li>
          The User indicates to create a new <em>&lt;whatever&gt;</em>.
        </li>
        <li>
          The System asks the User to enter the details of this new
          <em>&lt;whatever&gt;</em> according to the "Details" defined in
          the Associated Information of this use case.
        </li>
        <li>
          The User enters the details of this new
          <em>&lt;whatever&gt;</em> and confirms that she has finished.
        </li>
        <li>
          The System validates the User's inputs according to the "Details"
          defined in the Associated Information of this use case.
        </li>
        <li>
          The System validates that the creation of the new
          <em>&lt;whatever&gt;</em> will not duplicate any existing
          <em>&lt;whatever&gt;</em> according to the "Duplication detection
          rules" defined in the Associated Information of this use case.
        </li>
        <li>
          The System displays the details of the new
          <em>&lt;whatever&gt;</em> and asks the User to confirm the creation.
        </li>
        <li>
          The User either confirms the creation (continues the normal flow) or
          chooses to modify the details (return to step 3).
        </li>
        <li>
          The System saves the new <em>&lt;whatever&gt;</em> and informs the
          User that this <em>&lt;whatever&gt;</em> has been created.
        </li>
        <li>
          The System notifies relevant actors about the creation of the
          <em>&lt;whatever&gt;</em> according to the "Notification" defined in
          the Associated Information of this use case.
        </li>
        <li>Use case ends.</li>
      </ol>
    </td>
  </tr>
  <tr>
    <td>Extensions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      <b>4a. Input validation rule violation:</b> <br />
      4a1. The System alerts the User that an input validation rule is
      violated and displays the nature and location of the error.<br />
      4a2. The User corrects the mistake and returns to step 4 of the normal flow.<br />
      <b
        >5a. The System finds possible duplicates from the existing
        <em>&lt;whatever&gt;</em>s:</b
      ><br />
      5a1. The System alerts the User that the <em>&lt;whatever&gt;</em> she
      is trying to create already exists in the System.<br />
      5a2. <em>&lt;Specify how to handle it here&gt;</em>.<br />
      5a3. The User either chooses to correct the mistake and return to
      step 4 of the normal flow or chooses to terminate the use case.<br />
    </td>
  </tr>
  <tr>
    <td>Priority:</td>
    <td style="width: 80%; text-align: left" colspan="3">High</td>
  </tr>
  <tr>
    <td>Frequency of Use:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      Approximately *** user, average of *** usages per week.
    </td>
  </tr>
  <tr>
    <td>Business Rules:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      Security/access concerns
      <ul>
        <li>TBD</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>Associated Information:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      <table style="width: 100%">
        <tr>
          <th>Property name</th>
          <th>Data type</th>
          <th>Editability</th>
          <th>Validatoin rule</th>
          <th>Effect of change</th>
          <th>Reference to glossary</th>
        </tr>
        <tr>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
      </table>
      Column "Effect of change" shows consequences of modification other
      than saving. <br />
      Duplication detection rules:
      <ul>
        <li>
          Identifiers (A set of properties to prevent duplicate creation)
        </li>
      </ul>
      Notification:
      <ul>
        <li>Specify who to notify and what format</li>
      </ul>
      A basic set of commonly used constraints: <br />
      Checks that the input is not empty (empty means trimmed input length
      is 0). <br />
      Date:
      <ul>
        <li>Checks whether the input date is in a predefined format</li>
        <li>Checks whether the input date is in the future</li>
        <li>
          Checks whether the input date is in the present or in the future
        </li>
        <li>Checks whether the input date is in the past</li>
        <li>
          Checks whether the input date is in the past or in the present
        </li>
        <li>Checks whether the input date is in between a date range</li>
      </ul>
      Numeric value:
      <ul>
        <li>
          Checks whether the input value is less than or equal to the
          specified maximum
        </li>
        <li>
          Checks whether the input value is higher than or equal to the
          specified minimum
        </li>
        <li>
          Checks whether the input value is a number having up to certain
          number of digits and certain number of fractional digits
        </li>
        <li>
          Checks whether the input value is strictly positive. Zero values
          are considered invalid
        </li>
        <li>Checks whether the input value is positive or zero</li>
        <li>
          Checks whether the input value is strictly negative. Zero values
          are considered invalid
        </li>
        <li>Checks whether the input value is negative or zero</li>
        <li>
          Checks whether the input value is between min and max (inclusive)
        </li>
      </ul>
      Text:
      <ul>
        <li>
          Checks whether the specified character sequence's length is
          between min and max (inclusive)
        </li>
        <li>
          Checks whether the specified character sequence is a valid email
          address
        </li>
        <li>
          Checks whether the specified character sequence is a valid phone
          number
        </li>
        <li>
          Checks whether the specified string matches the provided regular
          expression
        </li>
      </ul>
      The User shall be able to cancel the use case at any time prior to
      submitting it.
    </td>
  </tr>
  <tr>
    <td>Related Use Cases:</td>
    <td style="width: 80%; text-align: left" colspan="3">
        The User may first choose to <ins>UC-01: Find <em>&lt;whatever&gt;</em>s</ins> but
      cannot find any, then decide to create one.
    </td>
  </tr>
  <tr>
    <td>Assumptions:</td>
    <td style="width: 80%; text-align: left" colspan="3"></td>
  </tr>
  <tr>
    <td>Open Issues:</td>
    <td style="width: 80%; text-align: left" colspan="3"></td>
  </tr>
</table>


See examples that adopt this template: [Use Case 1: Customer requests a SuperFrog appearance](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.roq29be23wgv) and [Use Case 13: Spirit Director creates account for a new SuperFrog Student](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.q9b056hngmki).

**[⬆ back to top](#table-of-contents)**

<a name="change-a-whatever"></a>
## 4. Change a *&lt;whatever&gt;*
<table style="text-align: right">
  <tr>
    <td>UC ID and Name:</td>
    <td style="width: 90%; text-align: left" colspan="3">
      UC-04: Change a <em>&lt;whatever&gt;</em>
    </td>
  </tr>
  <tr>
    <td>Created By:</td>
    <td style="width: 30%; text-align: left"></td>
    <td>Date Created:</td>
    <td style="width: 30%; text-align: left"></td>
  </tr>
  <tr>
    <td>Primary Actor:</td>
    <td style="width: 30%; text-align: left">User</td>
    <td>Secondary Actors:</td>
    <td style="width: 30%; text-align: left"></td>
  </tr>
  <tr>
    <td>Trigger:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      The User indicates to change the details of an existing
      <em>&lt;whatever&gt;</em>.
    </td>
  </tr>
  <tr>
    <td>Description:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      The User wants to change the details of an existing
      <em>&lt;whatever&gt;</em>, so that
      <em>&lt;rationale of this use case&gt;</em>.
    </td>
  </tr>
  <tr>
    <td>Preconditions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      PRE-1. The User is logged into the System. <br />
      PRE-2. The User has the "change" privilege. See the Business Rules of this
      use case. <br />
      PRE-3. <em>&lt;whatever&gt;</em> can be changed after the creation. <br />
    </td>
  </tr>
  <tr>
    <td>Postconditions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      POST-1. Changes made to the <em>&lt;whatever&gt;</em> are stored in
      the System.
    </td>
  </tr>
  <tr>
    <td>Main Success Scenario:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      <ol>
        <li>
          The User indicates to change the details of an existing
          <em>&lt;whatever&gt;</em>.
        </li>
        <li>
          The User views the details of this
          <em>&lt;whatever&gt;</em> through
          <u>UC-02: View a <em>&lt;whatever&gt;</em></u
          >.
        </li>
        <li>
          The User chooses to change the details of this
          <em>&lt;whatever&gt;</em>.
        </li>
        <li>
          The System asks the User to make changes to this
          <em>&lt;whatever&gt;</em> where allowed according to the "Details"
          defined in the Associated Information and the "Security/access concerns"
          defined in the Business Rules of this use case.
        </li>
        <li>
          The User makes changes to this <em>&lt;whatever&gt;</em> until she
          confirms that she has finished changing.
        </li>
        <li>
          The System validates the User's changes and alerts warning
          messages according to the "Details" defined in the Associated Information
          of this use case.
        </li>
        <li>The User acknowledges the warnings and chooses to continue.</li>
        <li>
          The System displays the updated details of this
          <em>&lt;whatever&gt;</em> and alerts the User to confirm the change.
        </li>
        <li>
          The User either confirms the change (continues the normal flow) or chooses
          to continue to change the details (return to step 5).
        </li>
        <li>
          The System saves the changes, carries out the effect of change
          according to the "Details" defined in the Associated Information of this
          use case, and informs the User that this
          <em>&lt;whatever&gt;</em> has been changed.
        </li>
        <li>
          The System notifies relevant actors about the change of
          <em>&lt;whatever&gt;</em> according to the "Notification" defined in
          the Associated Information of this use case.
        </li>
        <li>Use case ends.</li>
      </ol>
    </td>
  </tr>
  <tr>
    <td>Extensions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      <b>6a. Input validation rule violation:</b> <br />
      6a1. The System alerts the User that an input validation rule is
      violated and displays the nature and location of the error. <br />
      6a2. The User corrects the mistake and returns to step 6 of the normal flow.
    </td>
  </tr>
  <tr>
    <td>Priority:</td>
    <td style="width: 80%; text-align: left" colspan="3">High</td>
  </tr>
  <tr>
    <td>Frequency of Use:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      Approximately *** user, average of *** usages per week.
    </td>
  </tr>
  <tr>
    <td>Business Rules:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      Security/access concerns
      <ul>
        <li>TBD</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>Associated Information:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      <table style="width: 100%">
        <tr>
          <th>Property name</th>
          <th>Data type</th>
          <th>Editability</th>
          <th>Validatoin rule</th>
          <th>Effect of change</th>
          <th>Warning</th>
          <th>Reference to glossary</th>
        </tr>
        <tr>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
          <td></td>
        </tr>
      </table>
      Column "Effect of change" shows consequences of modification other
      than saving. <br />
      Notification:
      <ul>
        <li>Specify who to notify and what format</li>
      </ul>
      A basic set of commonly used constraints: <br />
      Checks that the input is not empty (empty means trimmed input length
      is 0). <br />
      Date:
      <ul>
        <li>Checks whether the input date is in a predefined format</li>
        <li>Checks whether the input date is in the future</li>
        <li>
          Checks whether the input date is in the present or in the future
        </li>
        <li>Checks whether the input date is in the past</li>
        <li>
          Checks whether the input date is in the past or in the present
        </li>
        <li>Checks whether the input date is in between a date range</li>
      </ul>
      Numeric value:
      <ul>
        <li>
          Checks whether the input value is less than or equal to the
          specified maximum
        </li>
        <li>
          Checks whether the input value is higher than or equal to the
          specified minimum
        </li>
        <li>
          Checks whether the input value is a number having up to certain
          number of digits and certain number of fractional digits
        </li>
        <li>
          Checks whether the input value is strictly positive. Zero values
          are considered invalid
        </li>
        <li>Checks whether the input value is positive or zero</li>
        <li>
          Checks whether the input value is strictly negative. Zero values
          are considered invalid
        </li>
        <li>Checks whether the input value is negative or zero</li>
        <li>
          Checks whether the input value is between min and max (inclusive)
        </li>
      </ul>
      Text:
      <ul>
        <li>
          Checks whether the specified character sequence's length is
          between min and max (inclusive)
        </li>
        <li>
          Checks whether the specified character sequence is a valid email
          address
        </li>
        <li>
          Checks whether the specified character sequence is a valid phone
          number
        </li>
        <li>
          Checks whether the specified string matches the provided regular
          expression
        </li>
      </ul>
      The User shall be able to cancel the use case at any time prior to
      submitting it.
    </td>
  </tr>
  <tr>
    <td>Related Use Cases:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      The User may first choose to UC-02: View a <em>&lt;whatever&gt;</em>,
      then decide to change one. <br />
      <em>[If the "Details" table contains an item which itself is a complex
      object (e.g., list), refer to UC: change an appearance. Similarly, in
      UC: change an appearance, refer to the UC: change a SuperFrog Student.
      <br />
      So a user may not change the detailed appearance in this use case, if a user
      wants to do that, she will need to go to UC-04: change an appearance.]</em>
    </td>
  </tr>
  <tr>
    <td>Assumptions:</td>
    <td style="width: 80%; text-align: left" colspan="3"></td>
  </tr>
  <tr>
    <td>Open Issues:</td>
    <td style="width: 80%; text-align: left" colspan="3"></td>
  </tr>
</table>


See examples that adopt this template: [Use Case 2: Customer edits request details](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.40n3tdbn3iga), [Use Case 8: Spirit Director edits basic information of a request](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.idpfgklhh6ju), and [Use Case 20: SuperFrog Student edits profile information](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.rapr7stw6a0b).

**[⬆ back to top](#table-of-contents)**

<a name="delete-a-whatevers"></a>
## 5. Delete a *&lt;whatever&gt;*
<table style="text-align: right">
  <tr>
    <td>UC ID and Name:</td>
    <td style="width: 90%; text-align: left" colspan="3">
      UC-05: Delete a <em>&lt;whatever&gt;</em>
    </td>
  </tr>
  <tr>
    <td>Created By:</td>
    <td style="width: 30%; text-align: left"></td>
    <td>Date Created:</td>
    <td style="width: 30%; text-align: left"></td>
  </tr>
  <tr>
    <td>Primary Actor:</td>
    <td style="width: 30%; text-align: left">User</td>
    <td>Secondary Actors:</td>
    <td style="width: 30%; text-align: left"></td>
  </tr>
  <tr>
    <td>Trigger:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      The User indicates to delete an existing
      <em>&lt;whatever&gt;</em>.
    </td>
  </tr>
  <tr>
    <td>Description:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      The User wants to delete an existing
      <em>&lt;whatever&gt;</em>, so that
      <em>&lt;rationale of this use case&gt;</em>.
    </td>
  </tr>
  <tr>
    <td>Preconditions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      PRE-1. The User is logged into the System. <br />
      PRE-2. The User has the "delete" privilege. See the Business Rules of this
      use case. <br />
      PRE-3. <em>&lt;whatever&gt;</em> can be deleted after the creation.
    </td>
  </tr>
  <tr>
    <td>Postconditions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      POST-1. The <em>&lt;whatever&gt;</em> is deleted from the System
      according to the "Deletion strategy" defined in the Associated Information of
      this use case.
    </td>
  </tr>
  <tr>
    <td>Main Success Scenario:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      <ol>
        <li>
          The User indicates to delete an existing
          <em>&lt;whatever&gt;</em>.
        </li>
        <li>
          The User views the details of this
          <em>&lt;whatever&gt;</em> through
          <u>UC-02: View a <em>&lt;whatever&gt;</em></u
          >.
        </li>
        <li>The User chooses to delete this <em>&lt;whatever&gt;</em>.</li>
        <li>
          The System validates that the deletion can be carried out
          according to the "Data integrity and deletion rules" and the "Referring
          objects handling strategy" defined in the Associated Information of
          this use case.
        </li>
        <li>
          The System alerts the User of the consequences of this deletion
          according to the "Data integrity and deletion rules" defined in
          the Associated Information of this use case, warns the User about the
          deletion, and asks the User to confirm.
        </li>
        <li>The User confirms the deletion.</li>
        <li>
          The System deletes the <em>&lt;whatever&gt;</em> according to
          the "Deletion strategy" and the "Referring objects handling strategy"
          defined in the Associated Information of this use case and alerts the
          User that this <em>&lt;whatever&gt;</em> has been deleted.
        </li>
        <li>
          The System notifies relevant actors about the deletion of
          <em>&lt;whatever&gt;</em> according to the "Notification" defined in
          the Associated Information of this use case.
        </li>
        <li>Use case ends.</li>
      </ol>
    </td>
  </tr>
  <tr>
    <td>Extensions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      <b>4a. Data integrity and deletion rule violation:</b> <br />
      4a1. The System alerts the User that a deletion rule is violated and
      displays the nature of the violation. <br />
      4a2. The System prompts possible actions to resolve the violation.
      <br />
      4a3. Use case terminates. <br />
    </td>
  </tr>
  <tr>
    <td>Priority:</td>
    <td style="width: 80%; text-align: left" colspan="3">High</td>
  </tr>
  <tr>
    <td>Frequency of Use:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      Approximately *** user, average of *** usages per week.
    </td>
  </tr>
  <tr>
    <td>Business Rules:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      Security/access concerns
      <ul>
        <li>TBD</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>Associated Information:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      Deletion strategy:
      <em>[<ul>
        <li>
          Physical delete: permanently remove the business domain object
          from the System (cannot be recovered)
        </li>
        <li>
          Move deleted object including any related objects that are being
          deleted along with it from the System to an archive or audit
          database
        </li>
        <li>
          Logic delete: mark a business domain object as "deleted" but still
          keep it in the live system, the deleted object will not be visible
          or available to all normal functions and users. Logically,
          "deleted" objects are not supposed to be "recovered" i.e., they
          will never be used again. Only special administrative users with
          privileged access can view them (Langlands, 2010)
        </li>
          </ul>]</em> <br/>
      Referring objects handling strategy: <br />
      Specify what action to take in respect of the related objects of
      <em>&lt;whatever&gt;</em> <br />
      <ul>
        <li>
          In case of composition:
          <ul>
            <li>
              Dependent objects are deleted along with
              <em>&lt;whatever&gt;</em>, aka cascading deletion
            </li>
            <li>
              The User needs to first delete dependent objects and then
              resume this use case
            </li>
          </ul>
        </li>
        <li>
          In case of regular association:
          <ul>
            <li>TBD</li>
          </ul>
        </li>
      </ul>
      <em>[Violation is more serious than warning. Violation will prevent the
      deletion and just terminate the use case, while the user can choose to
      ignore a warning and continue the use case. Please also list alert
       messages for each violation and warning.]</em> <br />
      Data integrity and deletion rules: <br />
      <ul>
        <li>
          Violation 1: <em>&lt;Detailed violation rule&gt;</em> See Business
          Rules of this use case
        </li>
        <li>
          Violation 2: <em>&lt;Detailed violation rule&gt;</em> See Business
          Rules of this use case
        </li>
        <li>...</li>
        <li>
          Referring objects handling strategy:
          <ul>
            <li>
              Warning 1: Dependent objects will be deleted along with
              <em>&lt;whatever&gt;</em>.
            </li>
            <li>
              Warning 2: Due to deletion, the referring objects will be left
              in limbo.
            </li>
            <li>...</li>
          </ul>
        </li>
      </ul>
      Notification: <br />
      <ul>
        <li>Specify who to notify and what format</li>
      </ul>
      The User shall be able to cancel the use case at any time prior to
      submitting it.
    </td>
  </tr>
  <tr>
    <td>Related Use Cases:</td>
    <td style="width: 80%; text-align: left" colspan="3">
        The User may first choose to <ins>UC-02: View a <em>&lt;whatever&gt;</em></ins>,
      then decide to delete one.<br />
    </td>
  </tr>
  <tr>
    <td>Assumptions:</td>
    <td style="width: 80%; text-align: left" colspan="3"></td>
  </tr>
  <tr>
    <td>Open Issues:</td>
    <td style="width: 80%; text-align: left" colspan="3"></td>
  </tr>
</table>


**[⬆ back to top](#table-of-contents)**

<a name="generate-a-report"></a>
## 6. Generate a *&lt;report type&gt;* report
<table style="text-align: right">
  <tr>
    <td>UC ID and Name:</td>
    <td style="width: 90%; text-align: left" colspan="3">
      UC-06: Generate a <em>&lt;report type&gt;</em> report
    </td>
  </tr>
  <tr>
    <td>Created By:</td>
    <td style="width: 30%; text-align: left"></td>
    <td>Date Created:</td>
    <td style="width: 30%; text-align: left"></td>
  </tr>
  <tr>
    <td>Primary Actor:</td>
      <td style="width: 30%; text-align: left">User <em>[Users who will generate the report or use it to make decisions]</em></td>
    <td>Secondary Actors:</td>
    <td style="width: 30%; text-align: left">
        Report recipient(s) <em>[Users who will generate the report or use it to make decisions]</em>
    </td>
  </tr>
  <tr>
    <td>Trigger:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      The User indicates to generate a <em>&lt;report type&gt;</em> report
      (on demand). <em>[If automatically, specify the triggering conditions or
        events and frequency (daily, weekly, monthly etc.) here.]</em>
    </td>
  </tr>
  <tr>
    <td>Description:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      The User wants to run a <em>&lt;report type&gt;</em> report, so that
      <em
        >&lt;purpose or business intent of the report: e.g., what business
        decisions will be made using information in the report, and by
        whom&gt;</em
      >.
    </td>
  </tr>
  <tr>
    <td>Preconditions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      PRE-1. The User is logged into the System. <br />
      PRE-2. The User has the "generate report" privilege. See the Business
      Rules of this use case.
    </td>
  </tr>
  <tr>
    <td>Postconditions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      POST-1. The details of the report are returned and displayed to the
      User.
    </td>
  </tr>
  <tr>
    <td>Main Success Scenario:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      <ol>
        <li>
          The User indicates to generate a <em>&lt;report type&gt;</em> report.
        </li>
        <li>
          The System asks the User to provide configurable report generating
          parameters according to the "Report generating parameters" defined in
          the Associated Information of this use case.
        </li>
        <li>
          The User enters the required parameters and confirms that she has
          finished entering.
        </li>
        <li>
          The System validates the input parameters according to the "Report
          generating parameters" defined in the Associated Information of this
          use case.
        </li>
        <li>
          The System generates the <em>&lt;report type&gt;</em> report
          according to the "Report generating algorithm" defined in
          the Associated Information of this use case and displays to the User
          according to the "Report generating parameters" defined in Associated
          Information of this use case.
        </li>
        <li>
          The System delivers the generated report according to the
          specified report disposition in the specified format in the "Report
          generating parameters" defined in the Associated Information of this
          use case.
        </li>
        <li>Use case ends.</li>
      </ol>
    </td>
  </tr>
  <tr>
    <td>Extensions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      <b>4a. Input validation rule violation:</b> <br />
      4b1. The System alerts the User that an input validation rule is
      violated and displays the nature and location of the error. <br />
      4b2. The User corrects the mistake and returns to step 4 of the normal flow. <br>
      <b>5a. No data is returned:</b> <br />
      5b1. The System alerts the User that no data is available in the
      generated report. <br />
      5b2. The User either chooses to return to step 3 of the normal flow or chooses to terminate
      the use case. <br>
      <b
        >6a. The User chooses to "Save report generating parameters" for
        future reuse:</b
      >
      <br />
      6a1. The System asks the User to enter a name for the current set of
      report generating parameters. <br />
      6a2. The User enters a name. <br />
      6a3. The System saves the name and the current set report generating
      parameters. <br />
      6a4. Use case resumes at the step of interruption.
    </td>
  </tr>
  <tr>
    <td>Priority:</td>
    <td style="width: 80%; text-align: left" colspan="3">High</td>
  </tr>
  <tr>
    <td>Frequency of Use:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      Approximately *** user, average of *** usages per week.
    </td>
  </tr>
  <tr>
    <td>Business Rules:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      Security/access concerns <br />
      <em>[Specify any limitations regarding which individuals, groups, or
      organizations are permitted to generate or view the report or which
      data they are permitted to select for inclusion. Identify any relevant
          business rules concerning security.]</em>
    </td>
  </tr>
  <tr>
    <td>Associated Information:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      Report generating parameters:
      <ul>
        <li>Report title</li>
        <li>
          Data source: The applications, files, databases, or data
          warehouses from which data will be extracted
        </li>
        <li>
          Data selection criteria (logic for what data to select and what to
          exclude)
        </li>
        <li>Columns/fields/properties to include</li>
        <li>
          Filter criteria used to restrict the report query prior to running
          the report
        </li>
        <li>Report visualization (table, charts, graph)</li>
        <li>Sorting criteria</li>
        <li>Pagination criteria if table visualization is selected</li>
        <li>
          Disposition of the report after it is generated. The options
          available will be displayed in the System, sent to a recipient,
          downloaded to local disk, printed, stored somewhere for future
          retrieval.
        </li>
        <li>
          Format of the generated report. The options available will be PDF,
          CSV, RTF, and HTML.
        </li>
      </ul>
      Report generating algorithm: <br />
      <em>[Specify how the report is generated based on user's input parameter.
      Specify calculations or other transformations that are performed to
          generate the data displayed.]</em>
    </td>
  </tr>
  <tr>
    <td>Related Use Cases:</td>
    <td style="width: 80%; text-align: left" colspan="3"></td>
  </tr>
  <tr>
    <td>Assumptions:</td>
    <td style="width: 80%; text-align: left" colspan="3">
      If the job is too large, the System prompts the User to select to run
      the report immediately or to schedule a time for it to run. The System
      will display a projected run time, based on historical run times.
    </td>
  </tr>
  <tr>
    <td>Open Issues:</td>
    <td style="width: 80%; text-align: left" colspan="3"></td>
  </tr>
</table>


See examples that adopt this template: [Use Case 18: Spirit Director generates TCU Honorarium (Payment for services) Request Forms](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.ff9ddug0ipbh) and [Use Case 19: Spirit Director generates a SuperFrog Students performance report](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit#bookmark=id.gswvt5fhug5k).

**[⬆ back to top](#table-of-contents)**
