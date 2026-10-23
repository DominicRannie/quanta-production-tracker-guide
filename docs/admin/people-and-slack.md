# People and Slack

The **People** table is everyone who can own a step: staff, and contractors such as PRX or the graphics designer. Writers and other outside contributors live in **Contributors** instead and never own steps.

## Add a person

Add a row with their name, email and roles. If they will own steps or receive alerts, add their **Slack member ID**.

## Slack member ID

Alerts are sent to a person's Slack member ID, not their name or email. To find it, in Slack open the person's profile, click the **⋯** menu and choose **Copy member ID**; it looks like `U04ABCDEFGH`. Paste it into the **Slack member ID** field on their row.

A person with steps but no ID gets no alerts; each automation run lists who was missed in its *missingSlack* output, so the gap is easy to spot.

## When someone leaves

Don't delete their row — their done steps point at it. Reassign their open steps (change the people fields on their pieces, or the step owners), change any **Default owner** that names them on the step templates, and clear their Slack member ID.
