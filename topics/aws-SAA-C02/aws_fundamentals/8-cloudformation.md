<h1>Cloudformation</h1>

Cloudformation is a tool that lets you create, update and delete infrastructure in AWS in consistent way using templates. So rather than creating and updating resources manually, you create a template and cloudformation will do the rest on your behalf.

A cloudformation template is written either in YAML or JSON.

All templates have a list of resources. Resources section of a template is only mandatory part of the cloudformation template.

Description field lets an author add description. It could be general information about template, cost of template, what the resources do etc.

If you have both fields (description and AwsTemplateFormatVersion) then the description field must immediately follow format version.

Metadata field has many functions but one of the things it does is it can control how the different things in AWS template are presented through the console UI. You can for example force and edit labels presented by the UI.

Parameters fields lets you add fields which prompt an user for more information for example ask user for which size of EC2 instance to use etc.

Mappings fields allows you to create look up tables for example you can map regions to specific AMIs.

Condition fields allow decision making in the templates so you can set certain things in the template that will only occur if a condition is met. It's a two way process as first you have to create a condition and then use it.

Outputs field allows you to present output messages once the templates are finished based on what has been created, finished or updated. For example it could return ID of an EC2 that's been created.

Cloudformation starts with a template which contains list of resources and other fields mentioned above. Resources inside cloudformation template are called logical resources. Logical resource has a type. They also generally have properties which cloudformation uses to configure the resources in certain way. When you take a template and give it to cloudformation then cloudformation creates what's known as "stack". Stack contains all of the logical resources that a template tells it to contains. Stack is a living and acting representation of a template. One template could create number of stacks. For any logical resources in a stack, cloudformation makes a corresponding physical resource in your AWS account. Updating logical resources in a stack will update corresponding physical resources in your AWS account. If you delete a stack all physical resources created from that stack will also be removed.