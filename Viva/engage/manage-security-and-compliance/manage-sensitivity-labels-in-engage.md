# Sensitivity labels in Viva Engage 

Sensitivity labels allow Engage community admins to protect and regulate access to sensitive organizational content created within those communities. After you configure sensitivity labels with their associated policies in the Microsoft Purview portal, these labels can be applied to communities in your organization.

## What's the difference between sensitivity labels and classification?

Sensitivity labels are different from Microsoft Entra group classification. Classifications are text strings that can be associated with a Microsoft 365 group but don't have any actual policies associated with them. You use classification as metadata and then must use other methods such as internal tools and scripts to enforce policies.

The benefit of using sensitivity labels is that their policies are automatically enforced end-to-end through a combination of the Microsoft 365 Groups platform, the Microsoft Purview portal, and Engage. Sensitivity labels provide powerful infrastructure support for securing your organization's sensitive data and ensuring compliance with your internal policies or regulations.

If you currently use classification, see the following documentation for more information and instructions how to convert these values to sensitivity labels: Classic Microsoft Entra group classification.

## Engage is a public-first platform in our organization. Is it possible to continue that practice with sensitivity labels?

A preferred default label for Engage communities can be selected in Microsoft Purview as part of the label policy settings. This default will take precedence over the default label for sites. For example, you may have a sensitivity label of "General" that has the label privacy option configured as **Public** and a sensitivity label of "Confidential" that has the label privacy option configured as **Private**. You can choose the “General” label as your Engage default label and the “Confidential” label as your site default label. Users creating new sites will see the sensitivity drop-down pre-populated with the “Confidential” label, while it will be pre-populated with the “General” label when users create a new Engage community.

## Example scenarios for sensitivity labels

### Set the privacy level for communities

You can create and configure a sensitivity label that, when applied during community creation, allows users to create communities with a specific privacy (public or private) setting.
For example, you create and publish a sensitivity label named "Confidential" that has the label privacy option configured as **Private**. As a result, any community that's created with this label must be a private community.
When a user creates a new creation and selects the Confidential label, the only privacy option that's available to the user is Private:
[[unsure how/where to embed image but I have it]]

Similarly, you create and publish a sensitivity label named "General" that has the label privacy option configured as **Public**. When a user creates a new community, they have a choice of privacy options:
[[another screenshot]]

When the community is created, the sensitivity label is visible to users in the lower-right corner of the community header.
[[third screenshot]]

A community admin can change the sensitivity label and the privacy setting of the community at any time by going to the community, clicking the **…** button, and choosing **Settings**.
[[fourth screenshot]]

### Control guest access to communities

You can use sensitivity labels to control guest access to your communities. Communities created with a label that doesn't allow guest access are only available to users in your organization. People outside your organization can't be added to the community.

## Limitations

Before you use sensitivity labels for Engage, be aware of the following limitation:
- **Sensitivity labels aren’t directly supported by PowerShell cmdlets**
  Users won’t be able to specify sensitivity labels directly for Engage communities. However, it is possible to use PowerShell to apply labels to the SharePoint site connected to your existing Engage community, which will cause the label on the Engage community to be updated as well.

## How to create and configure sensitivity labels for Engage

Use the full documentation from Microsoft Purview for information about creating and configuring sensitivity labels:
- [[link]]
