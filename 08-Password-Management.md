# Password Management

## 1. What Is Password Management?

**Password Management** is an optional add-on for SailPoint Identity Security Cloud (ISC) that simplifies password administration and supports password updates across connected account sources and applications.

It helps organisations manage password-related activities centrally and enforce consistent password policies across their environment.

### Why Is It Used?

Organisations often have users accessing multiple applications and systems, each of which may have its own password requirements.

Without centralised password management, users and administrators may need to manage password changes separately across different systems.

ISC Password Management helps address this by supporting:

- **Centralised password administration:** Simplifies password-related operations across connected sources.
- **Consistent password policies:** Helps enforce strong and consistent password requirements.
- **Password updates across applications:** Supports password changes across configured account sources and applications.
- **Improved security:** Allows organisations to apply additional security controls before permitting password changes.

**Important:** Password Management is an optional ISC add-on. It should not be confused with the core provisioning functionality.

## 2. Password Change Process

A password change process begins after a user has authenticated to ISC and initiates a password-change request.

However, successful authentication alone does not necessarily mean the user should immediately be allowed to change their password.

Password changes are security-sensitive operations. An organisation can configure additional verification requirements before allowing the request to proceed.

### Why Is Additional Verification Necessary?

If an attacker gains access to a user's authenticated session, they may attempt to change the account password and take control of the account.

To reduce this risk, ISC can treat password changes as security events and enforce stronger verification controls.

For example, an organisation can require users to complete a **strong authentication challenge** before submitting a password-change request.

This adds another layer of protection beyond the initial login.

## 3. Password Change Security Flow

The conceptual flow is:

1. **User authentication:** The user authenticates to ISC.
2. **Password-change initiation:** The user begins a password-change request.
3. **Additional security verification:** ISC can require a strong authentication challenge before allowing the request to proceed.
4. **Password change:** Once the required verification is satisfied, the password-change process can continue.

The exact verification and fulfilment steps depend on the configured password-management capabilities and connected sources.

## 4. Key Concepts

| Term | Meaning |
|---|---|
| Password Management | Optional ISC add-on for simplifying password administration and updates. |
| Password Change | A process initiated by an authenticated user to change a password. |
| Strong Authentication Challenge | An additional verification requirement that can be enforced before a password-change request is submitted. |
| Password Policy | Rules governing password requirements, such as strength and complexity. |

## 5. Password Management and Provisioning

Password Management and provisioning are related, but they are not interchangeable.

| Password Management | Provisioning |
|---|---|
| Focuses on password administration and password changes. | Focuses on applying account and access changes. |
| Supports password policy enforcement and additional verification controls. | Handles operations such as creating accounts, modifying attributes, and granting or removing access. |
| Available as an optional ISC add-on. | A core identity governance process. |

A password change can involve communication with connected account sources, but password management is the specialised capability for managing password-related operations.

## Key Takeaways

- Password Management is an optional Identity Security Cloud add-on.
- It simplifies password administration and supports password updates across connected sources and applications.
- Organisations can use it to enforce consistent and strong password policies.
- A password-change request begins after the user authenticates to ISC.
- Additional strong authentication can be required before the user is allowed to submit a password-change request.
- Password changes should be treated as security-sensitive operations.
