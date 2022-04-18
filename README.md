# A Practical Style Guide and Templates Repository for Writing Effective Use Cases

*An opinionated style guide for use case writing*

Software developers are most effective when handed with a set of consistent and self-contained use cases. However, writing high-quality use cases is a difficult and time-consuming task. Inspired by the success of various coding style guides, we developed a use case writing style guide and a small set of use case templates to slightly constrain the way a use case is written. This style guide will help reduce excessive personal idiosyncrasy in use case writing and give a uniform appearance to the use case written by different requirements engineers so that it is much easier to understand a large set of use cases. 

Instead of overly restricting the use case writing process, the purpose of this style guide is to find a balance between readability and creativity.

> **Note**: The use case templates repository is available at [here](./use-case-templates/README.md). A real project's use case specification following this style guide is available at [here](https://docs.google.com/document/d/1PBDgqCbMPpyrAWZnob_OxDecOPoyyOtV_sJeeObh62E/edit?usp=sharing). Feel free to provide feedback.

## Table of contents

1. [Generic use case specification format](#generic-use-case-specification-format)
2. [Use case naming](#use-case-naming)
3. [Actors](#actors)
4. [Trigger](#trigger)
5. [Use case description](#use-case-description)
6. [Action steps](#action-steps)
7. [Extensions](#extensions)
8. [Data requirements](#data-requirements)
9. [Business rules](#business-rules)
10. [Related use cases](#related-use-cases)
11. [Amendments](#amendments)

<a name="generic-use-case-specification-format"></a>
## 1. Generic use case specification format

<a name="generic-use-case-specification-format--syntax"></a><a name="1.1"></a>

  - [1.1](#generic-use-case-specification-format--syntax) We adopt the use case specification format from [Software Requirements (Third Edition)](https://www.microsoftpressstore.com/store/software-requirements-9780735679665) by Karl Wiegers and Joy Beatty with slight modification as a basis for writing use cases.
<table style="width:100%; text-align: right;">
  <tr>
    <td>UC ID and Name:</td>
    <td style="width:60%" colspan="3"> &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;</td>
  </tr>
  <tr>
    <td>Created By:</td>
    <td style="width:18%">&emsp;&emsp;&emsp;&emsp;</td>
    <td>Date Created:</td>
    <td style="width:18%">&emsp;&emsp;&emsp;&emsp;</td>
  </tr>
  <tr>
    <td>Primary Actor:</td>
    <td style="width:18%">&emsp;&emsp;&emsp;&emsp;</td>
    <td>Secondary Actors:</td>
    <td style="width:18%">&emsp;&emsp;&emsp;&emsp;</td>
  </tr>
  <tr>
    <td>Trigger:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Description:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Preconditions:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Postconditions:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Main Success Scenario:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Extensions:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Priority:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Frequency of Use:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Business Rules:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Associated Information:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Related Use Cases:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Assumptions:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
  <tr>
    <td>Open Issues:</td>
    <td style="width:60%" colspan="3"></td>
  </tr>
</table>



**[⬆ back to top](#table-of-contents)**

<a name="use-case-naming"></a>
## 2. Use case naming
  <a name="use-case-naming--id"></a><a name="2.1"></a>
  - [2.1](#use-case-naming--id) Assign a unique ID to each use case.
    > Rationale: This ensures that you can quickly identify one use case.

  <a name="use-case-naming--verb"></a><a name="2.2"></a>
  - [2.2](#use-case-naming--verb) Start with a verb with the first letter capitalized and describe the goal of the user.
    - Positive example: UC-03: Request a SuperFrog appearance for TCU events
    - Negative example: SuperFrog appearance request management

**[⬆ back to top](#table-of-contents)**

<a name="actors"></a>
## 3. Actors
An actor specifies a role played by a user or any other system that interacts with the system under development. 
  <a name="actors--name"></a><a name="3.1"></a>
  - [3.1](#actors--name) Use a singular substantive name. To highlight this characteristic, capitalize the actor's name.
    - Positive example: The Spirit Team Director *&lt;completes a task&gt;*.
    - Negative example: The spirit team director *&lt;completes a task&gt;*.

  <a name="actors--all"></a><a name="3.4"></a>
  - [3.2](#actors--all) Include all actors participating in the use case.
    > Note: Many use cases neglect to include some important secondary actors.

**[⬆ back to top](#table-of-contents)**

<a name="trigger"></a>
## 4. Trigger
A trigger is the initiator of a use case.
  <a name="trigger--syntax"></a><a name="4.1"></a>
  - [4.1](#trigger--syntax) Use "The *&lt;Primary Actor&gt;* indicates to do . . . " or "The *&lt;Primary Actor&gt;* chooses to do . . . " to describe the trigger of the use case.
    - Positive example: The User indicates to search for products meeting defined search criteria.
    - Positive example: The User chooses to search for products meeting defined search criteria.

  <a name="trigger--first-action-step"></a><a name="4.2"></a>
  - [4.2](#trigger--first-action-step) Trigger is the same as the first action step in the main success scenario.

  <a name="trigger--more-than-one"></a><a name="4.3"></a>
  - [4.3](#trigger--more-than-one) If a use case has more than one trigger, pick one as the trigger and the first action step of the main success scenario and treat others as the extensions of the first action step.
    - For example, use case "Cancel a request" can be triggered either by the Spirit Director or by time, because one business rule states: "If a payment is not received 24 hours prior to the event date and time, request will be automatically canceled." In this case, we will make the human trigger as the first step in the main success scenario, "1. The Spirit Director indicates to cancel a request." Then in the extension section of the use case, we use "1a. Payment is not received 24 hours prior to the event date and time." to start an alternative success scenario.

**[⬆ back to top](#table-of-contents)**

<a name="use-case-description"></a>
## 5. Use case description
We require a one-sentence description for each use case.
  <a name="use-case-description--required"></a><a name="5.1"></a>
  - [5.1](#use-case-description--required) Use "The *&lt;Primary Actor&gt;* wants to *&lt;completes a task&gt;* so that *&lt;goal and rationale&gt;*" to describe the gist of the use case in one sentence.
    > Rationale: Use case description works as a summary of the use case. It is read by busy people.

**[⬆ back to top](#table-of-contents)**

<a name="action-steps"></a>
## 6. Action steps
Use case action steps are sentences that form a use case's main success scenario and extensions. According to [Alistair Cockburn](https://g.co/kgs/Hy777n), a use case action step either describes an interaction between two actors e.g., "The Customer enters address information." or a validation step to protect interest of a stakeholder e.g., "The System validates the credentials." or an internal change to satisfy a stakeholder e.g., "The System deducts amount from balance." Our style guide complements Cockburn's classic 10 action step writing guidelines by recommending proper words and sentence structures.

  <a name="action-steps--primary-actor-intention"></a><a name="6.1"></a>
  - [6.1](#action-steps--primary-actor-intention) Use the following wording and sentence structure to describe the Primary Actor's intention (Corresponds to Cockburn's interaction between two actors)
    - The *&lt;Primary Actor&gt;* indicates to/selects to/chooses to/requests to/attempts to . . .
    - The *&lt;Primary Actor&gt;* submits . . .
    - The *&lt;Primary Actor&gt;* views . . .
    - The *&lt;Primary Actor&gt;* verifies . . . and confirms . . .
    - The *&lt;Primary Actor&gt;* enters/provides/specifies . . . and confirms she has finished entering.
    - The *&lt;Primary Actor&gt;* continues entering . . .
    - The *&lt;Primary Actor&gt;* . . . until confirming that she has finished . . .
    - The *&lt;Primary Actor&gt;* acknowledges . . . (e.g., the alert or warning) and confirms to continue.
    - The *&lt;Primary Actor&gt;* ignores the warning/alarm and confirms to continue.

  <a name="action-steps--systen-internal-processing"></a><a name="6.2"></a>
  - [6.2](#action-steps--systen-internal-processing) Use the following wording and sentence structure to describe the system internal processing (Corresponds to Cockburn's validation step and internal change)
    - The System validates, saves, records, calculates, updates, deletes, creates, retrieves, triggers ...

  <a name="action-steps--system-interaction"></a><a name="6.3"></a>
  - [6.3](#action-steps--system-interaction) Use the following wording and sentence structure to describe an interaction started by the System (Corresponds to Cockburn's interaction between two actors)
    - The System displays/shows/presents/informs . . . according to . . . defined in the Associated Information of this use case. (This is usually the information retrieved from a data source. For example, a list of products or a graph of stats. The previous action step may be "The System retrieves . . . ")
    - The System alerts/warns/alarms . . . (This is used when something is about to break the business rule, or something is about the change the state of the system, usually occurs in extensions.)
    - The System asks the *&lt;Primary Actor&gt;* to enter . . . according to . . . defined in Associated Information of this use case.
    - The System prompts the *&lt;Primary Actor&gt;* . . . (The system knows some information that would help the user decide what to do next) or The System offers . . . options/methods/choices . . .
    - The System notifies/sends *&lt;Secondary Actors&gt;* ...

  <a name="action-steps--system-to-system-interaction"></a><a name="6.4"></a>
  - [6.4](#action-steps--system-to-system-interaction) Use the following wording and sentence structure to describe an interaction between the System and another system in the environment (Corresponds to Cockburn's interaction between two actors)
    - The System has another system do something.

  <a name="action-steps--system-feedback"></a><a name="6.5"></a>
  - [6.5](#action-steps--system-feedback) The System always provides feedback that the requested task has been finished. This allows the User to know the command has been completed, even if it is not immediately obvious.
    - Positive example: The System indicates that the calculation is finished.

  <a name="action-steps--user-feedback"></a><a name="6.6"></a>
  - [6.6](#action-steps--user-feedback) The User always provides feedback to the System.
    - Positive example: The User confirms that the . . . is complete.
    - Positive example: The System processes . . . and indicates to the User . . . , then the User acknowledges the indication.

  <a name="action-steps--first-step"></a><a name="6.7"></a>
  - [6.7](#action-steps--first-step) The first sentence in the main success scenario must report the event that activates the execution of the functionality described in the use case.

  <a name="action-steps--end-step"></a><a name="6.8"></a>
  - [6.8](#action-steps--end-step) Use "Use case ends." to explicitly indicate the end of a use case.

  <a name="action-steps--include-use-case"></a><a name="6.9"></a>
  - [6.9](#action-steps--include-use-case) When including another use case, use "The User or System *&lt;completes a task&gt;* through <ins>UC-*&lt;ID&gt;*: *&lt;Use Case Name&gt;*</ins>."

**[⬆ back to top](#table-of-contents)**

<a name="extensions"></a>
## 7. Extensions
An extension describes either an exception of a step in the main success scenario or an alternative success scenario.
  <a name="extensions--syntax"></a><a name="7.1"></a>
  - [7.1](#extensions--syntax) Use the following wording and sentence structure to describe the handling of use case extensions.
    - The System alerts the *&lt;Primary Actor&gt;* that an input validation rule is violated and displays the nature and location of the error.
    - The *&lt;Primary Actor&gt;* corrects the mistake, then returns to step . . . of normal flow.
    - The *&lt;Primary Actor&gt;* chooses to terminate the use case.

**[⬆ back to top](#table-of-contents)**

<a name="data-requirements"></a>
## 8. Data requirements
It is recommended to include data requirements when specifying a use case. We use terminologies like "details" or "property lists" to denote data requirements.
  <a name="data-requirements--syntax"></a><a name="8.1"></a>

  - [8.1](#data-requirements--syntax) Use tabular format to describe the Primary Actor's input and the System's output data in Associated Information section of a use case . Each row describes one detail or property. Each column represents one characteristic of interest to the action steps in the use case.

    | Property name | Data type | Changeability | Validation rule | Glossary |
    | ------------- | --------- | ------------- | --------------- | -------- |
    |               |           |               |                 |          |

**[⬆ back to top](#table-of-contents)**

<a name="business-rules"></a>
## 9. Business rules
Business rules include corporate policies, government regulations, laws, industry standards, and computational algorithms.
  <a name="business-rules--syntax"></a><a name="9.1"></a>

  - [9.1](#business-rules--syntax) Specify related business rules (e.g., security and access control requirements) in the business rules section.
    - Identify any relevant business rules concerning security/access.
    - Specify more finer-grained access control.
    - Specify any limitations regarding which individuals, groups, or organizations are permitted to initiate this use case or which data they are permitted to access.

**[⬆ back to top](#table-of-contents)**

<a name="related-use-cases"></a>
## 10. Related use cases
  <a name="related-use-cases--required"></a><a name="10.1"></a>
  - [10.1](#related-use-cases--required) Provide related use cases.
    > Rationale: This is incredibly useful for software architecture design and UI design. E.g., "View a *&lt;whatever&gt;*" is related to "Find *&lt;whatever&gt;*s."

**[⬆ back to top](#table-of-contents)**

<a name="amendments"></a>
## 11. Amendments
We encourage you to fork this guide and change the rules to fit your team's use case writing style guide. Below, you may list some amendments to the style guide. This allows you to periodically update your style guide without having to deal with merge conflicts.
**[⬆ back to top](#table-of-contents)**
