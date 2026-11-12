# Provisioning

## 1. What Is Provisioning?

**Provisioning** is the process of granting, modifying, or removing a user's access to systems, applications, and databases based on their identity and access requirements.

In Identity Security Cloud (ISC), provisioning translates an identity-related decision into an actual change on a connected source.

For example:

- A new employee joins and needs an account in the company's email system.
- An employee moves to another department and needs different application permissions.
- An employee leaves the organisation and their access must be removed.

In each case, provisioning helps ensure that the required access changes are carried out on the relevant systems.

> **Remember:** Provisioning is not limited to creating accounts. It also includes updating existing accounts, assigning or removing access, and changing account attributes.

## 2. How Provisioning Works

Whenever ISC communicates with a connected source to make an access or account-data change, it is performing a provisioning operation.

The process can be understood through four stages:

### Provisioning Workflow

| Stage | What happens |
|---|---|
| 1. Trigger Provisioning | An event or user action creates a need for a data or access change. |
| 2. Package the Plan | ISC prepares a plan describing the required operations and data changes. |
| 3. Manage Fulfilment | ISC sends the change to a connected source or routes it for manual fulfilment. |
| 4. Verify the Change | Data is aggregated again so ISC can verify whether the requested change took effect. |

### Stage 1: Trigger Provisioning

Provisioning begins when an event creates a requirement to change account data or access.

The trigger may be:

- **Automated:** An identity attribute changes, a lifecycle state changes, or role-assignment logic determines that access must be updated.
- **User-initiated:** A user requests access, submits a password-change request, or a certification decision results in access being revoked.

The trigger establishes *what needs to change*. It does not necessarily mean the change has already been applied.

### Stage 2: Package the Plan

ISC packages the requested changes into a **provisioning plan**.

A provisioning plan describes the operations and data that need to be communicated to the relevant systems.

For example, when an employee moves from Finance to HR, the plan may contain operations to:

- Remove access associated with the employee's previous responsibilities.
- Add the access required for the new role.
- Update relevant account attributes.

The plan provides a structured way for ISC to communicate the required changes.

### Stage 3: Manage Fulfilment

ISC sends the provisioning request for fulfilment.

There are two broad approaches:

| Fulfilment method | Explanation |
|---|---|
| Automated fulfilment | ISC communicates directly with a connected source, which processes the requested change. |
| Manual fulfilment | ISC sends a notification or task to an external ticketing system or an individual who must complete the change manually. |

**Example:** If an application supports automated provisioning, ISC may send the required account update directly. If it does not, a task may be sent to an administrator through an external ticketing system.

The exact fulfilment method depends on the source, its configuration, and the available integration capabilities.

### Stage 4: Verify the Change

After fulfilment, the source's data is aggregated again into ISC.

This allows ISC to compare the resulting account information with the intended change and verify whether the requested update took effect.

**Important distinction:** Sending a provisioning request does not, by itself, prove that the target system successfully applied the change. Verification provides a way to check the resulting state.

## 3. What Triggers Provisioning?

ISC supports two broad categories of provisioning triggers.

### A. Data-driven or Automated Triggers

These triggers occur when identity data or governance-related conditions change.

Examples include:

- **Lifecycle state changes:** A user's lifecycle state changes, and the associated access configuration triggers provisioning.
- **Role assignment:** A user is assigned or removed from a role, resulting in corresponding access changes.
- **Attribute synchronisation:** Changes to selected identity attributes are propagated to other systems to keep information consistent.

**Example:**

An employee's department changes from Finance to Human Resources.

1. The identity record is updated.
2. ISC evaluates the applicable lifecycle state and role-assignment logic.
3. The required access changes are identified.
4. Provisioning communicates those changes to the relevant sources.

### B. Request-driven or User-initiated Triggers

These triggers begin when a user or another authorised participant initiates an action.

Examples include:

- **Access requests:** A user requests a role, access profile, or entitlement. Once any required approvals are completed, the requested access can be provisioned.
- **Password changes:** A user submits a password-change request that results in a change on a connected system.
- **Certification revocations:** A reviewer decides that access should be revoked during an access certification. The resulting removal is handled through provisioning.

**Important:** Not every access request requires approval. Approval requirements depend on the configuration of the requested access.

## 4. Provisioning in the Identity Lifecycle

Provisioning supports changes throughout a user's relationship with an organisation.

| Lifecycle event | Possible provisioning activity |
|---|---|
| Joiner | Create accounts and grant initial access. |
| Mover | Modify existing access to reflect a new role, department, or responsibility. |
| Leaver | Disable or remove accounts and revoke access. |

This is commonly described as **Joiner-Mover-Leaver (JML) provisioning**.

The objective is to ensure that access changes as a person's organisational responsibilities change, rather than remaining static.

## 5. Key Terms

| Term | Meaning |
|---|---|
| Provisioning | Applying account or access changes to connected systems. |
| Trigger | An event or action that initiates a provisioning requirement. |
| Provisioning plan | A structured description of the operations and data changes ISC needs to communicate. |
| Fulfilment | Carrying out the requested changes on the target system, automatically or manually. |
| Aggregation | Collecting account and entitlement data from connected sources into ISC. |
| Verification | Checking the aggregated data to determine whether the intended change took effect. |

## 6. Provisioning vs. Access Requests vs. Access Certifications

These concepts are related, but they serve different purposes.

| Concept | Main purpose | Example |
|---|---|---|
| Access Request | Allows someone to request access. | An employee requests access to a Finance application. |
| Access Certification | Allows a reviewer to decide whether existing access should be retained or revoked. | A manager revokes unnecessary Finance access. |
| Provisioning | Carries out the resulting account or access change. | ISC sends the instruction to remove the employee's Finance access. |

**The relationship:** An access request or certification decision may trigger provisioning, but provisioning is the process that fulfils the resulting change.

## Key Takeaways

- Provisioning translates identity and access decisions into changes on connected systems.
- It covers granting, modifying, and removing access, not just account creation.
- The four stages are Trigger, Package the Plan, Manage Fulfilment, and Verify the Change.
- Provisioning can be triggered by automated identity changes or user-initiated actions.
- Fulfilment can be automated through a connected source or handled manually.
- Aggregation after fulfilment helps ISC verify the resulting account data.
- Provisioning supports Joiner-Mover-Leaver processes and ongoing access governance.
