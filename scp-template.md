# Security Check Proposal [Template]

This is the suggested template for new Security Check Proposals (SCPs).

## Check

The content of security check that would be added to SCSVS. The check should be imperative and describe an action to be performed.

Example: _Verify that if the implemented functions include external calls, they are handled correctly and do not introduce unsafe external calls to the system._

There should be only one proposed check, unless the aim of the proposal is to introduce a new category.

## Chapter & category

SCSVS chapter and category that the check should be added to. This section should also describe why this category is selected. 

Example: _C1: Token_

### New category

The "Chapter & category" section can introduce new categories, but the proposal should include the motivation, rationale and more than one check for the proposed category.

## Motivation & rationale

The motivation section should describe the "why" of this security check. What potential security bug does it protect from? What benefit does it provide to the protocol? What functionality and use cases does this check address?

## Real-life example (optional)

This section (optional but welcomed) should describe a real case of the security bug that the check refers to. Verifying the proposed check should protect from the security bug in the addressed real-life example.

## References

External references to sites which describe the addressed security bug, proposed protection, best practices, post-mortems, etc.

The aim of this section from the reader's perspective is to get to know the further details of the addressed issue.

## Pull Request (optional)

This section is optional but **very** welcomed and should contain a link to a Pull Request that adds the check to SCSVS.

## License

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.