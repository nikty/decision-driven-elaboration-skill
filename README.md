# Decision-Driven Elaboration

EN | [RU](./README.ru.md)

**Decision-Driven Elaboration** is a skill for systematically defining product or system functionality through explicit behavioral decisions.

Instead of generating a specification immediately, the skill identifies important ambiguities and helps resolve them one at a time. It asks **one question at a time**, presents 2–3 alternatives, explains their implications, and provides a recommendation. Agreed decisions are recorded and used throughout the discussion.

On request, the skill converts agreed decisions into **testable requirements using EARS syntax**, without inventing behavior that has not been explicitly defined.

## Usage Example

**User:**
> Use @Decision-Driven Elaboration. I want to design an automatic configuration saving mechanism for a network device.

**Assistant:**
> Let's start with when the configuration should be saved.
>
> **A.** Save every change immediately. Minimal risk of data loss, but more write operations.
>
> **B.** Save changes after a period of inactivity. Fewer write operations, but recent changes may be lost.
>
> **Recommendation:** B, if a short saving delay is acceptable.
>
> Which option do you prefer?

**User:**
> B. Use a 30-second delay.

**Assistant:**
> **Agreed:** The configuration is automatically saved 30 seconds after the last change.
>
> Next question: What should happen if the device reboots before the delay expires?
>
> **A.** Save pending changes before rebooting.
>
> **B.** Reboot without saving pending changes.
>
> **Recommendation:** A, to prevent configuration loss.

The discussion continues until all significant behavioral decisions are resolved. The user can then request a formal specification:

> Generate EARS requirements based on the agreed decisions.
