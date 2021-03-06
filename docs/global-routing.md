# Routing Global
**Management :material-menu-right: Routing Global**

**Routing Global** allows you to create routing templates that can be applied to multiple customers. This is ideal when all or multiple customers are using a repeatable configuration, either the same type of route or the same routing settings. When you need to apply a change to routing for multiple customers, you only need to update the template. 

## Create Global Routing
To setup a **Routing Global** template, first create it then apply it to the customer account(s) using the **Tag** field. 

**Step 1: Create the template**

2. Click the **:material-menu-right:** to create a new template
3. For complete field descriptions, see [**Ingress Routing configuration**](https://docs.connexcs.com/customer/routing/#configure-routing).

    ![alt text][routing-global]

4. The **Tag** field is essentially the name of the template. When customer routing is setup using the template, the Tag will be visible in **Customer :material-menu-right: Edit :material-menu-right: Config :material-menu-right: Tags**.
5. Select **`Save`**.

**Step 2: Assign the template**

For each customer that needs the new template:

1. Navigate to **Management :material-menu-right: Customer** and select the customer
2. Select **`Edit`** in the upper right corner
3. On the Config tab, select the new template under **Tags**
4. Save the customer configuration. 

!!! info "Using Routing Global and Script Forge"
    Routing Global templates can't be used to set routing details with ScriptForge (Vars box). With appropriate design, these can be configured directly under Customer Routing.

[routing-global]: /misc/img/routing-global.png "Edit Global Routing"
