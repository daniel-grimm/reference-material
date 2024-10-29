Power Apps are Microsoft's no code / low code solution.

Power Apps comes in two main flavors Canvas apps, and Model Driven Apps.

Power Apps also have strong integration and automation capabilities. There are dozens of integrations with Teams, Outlook, Sharepoint, and non-Microsoft offerings that enable advanced capabilities. Power Automate can also be integrated to allow actions to occur automatically based on triggers.

# Canvas Apps
Canvas driven apps give the developer complete control over the UI and data of the application.

Canvas apps are being left behind in favor of the Model Driven architecutre due to the rigors of enforcing an object structure.

# Model Driven Apps
Model Driven Apps are more structured, where the user defines the data structure, before adding UI and additional controls, albeit in a more limited fashion than a Canvas app.

Model Driven Apps provide pre-packaged components that can be drag and dropped to create interactive forms to capture user data and insert it into Microsoft Datavers.

Models can have rules and validation applied using Business Rules. These rules are applied dynamically as the user goes through the form. These rules can be activated or deactivated separately from the columns to make the changes apply immediately.

What if you want to create complex data structures? Dataverse supports that! You can create Many-to-one and Many-to-Many relationships between tables to connect information together.

# Power Automation
Power Automation lets you create workflows using a library of plugins. Merely enter in a trigger condition, and fill out the parameters for each plugin and workloads will be automatically created.

These automations can be triggered manually, or automatically. Automated triggers fall into two categories: Scheduled, and automated. The scheduled flows will execute on a set schedule, the automated flows will trigger when a condition is met.

Most of the third party plugins require a premium (paid) tier of service, but even the Microsoft native plugins are pretty powerful.

## Shortcomings
References to other tables in Dataverse is a bit mysterious. Not all data types can be referenced via formula. For instance Text can be referred to via formula, but Email, which is a sub-type of Text, cannot be referenced.

I find a feature of Power Apps to also be a flaw. If you have a column that is a part of a form or process or flow, you cannot delete the column without first removing the reference and republishing. This is a huge headache when wanting to do something as simple as changing the sub-type of the column. This can cause extensive menial re-work as you delete all references, change the type, and then re-add all the references in the application.
