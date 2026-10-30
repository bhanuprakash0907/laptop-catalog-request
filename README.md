# ServiceNow Project: Laptop Request Catalog Item

## Project Overview

The **Laptop Request Catalog Item** simplifies and automates laptop requests within an organization. Instead of relying on manual requests that can cause delays, missing information, and inefficiencies, employees use a structured form in the ServiceNow Service Catalog.

The form adapts to user input, uses UI Policies to enforce requirements, and includes a reset option for convenience.

## Key Features

- **Laptop Request catalog item** available under the **Hardware** category.
- **Catalog variables:**
  - `Laptop Model` — single-line text.
  - `Justification` — multi-line text describing the request.
  - `Additional Accessories` — checkbox.
  - `Accessories Details` — shown and required when accessories are selected.
- **UI Policy and UI Policy Action** to show or hide dependent fields and enforce required fields.
- **Reset Form UI Action** to clear the form without refreshing the page.
- **Update Set** exported as XML for moving the configuration between ServiceNow instances.

## Setup and Use

### 1. Import the Update Set

1. In ServiceNow, go to **All → System Update Sets → Retrieved Update Sets**.
2. Select **Import Update Set from XML**.
3. Upload `Laptop_Request_UpdateSet.xml`.
4. Select **Preview Update Set**, review the preview, then select **Commit Update Set**.

### 2. Open the Catalog Item

1. Go to **Service Catalog → Hardware**.
2. Open **Laptop Request**.
3. Enter the laptop model and justification, and indicate whether accessories are needed.

### 3. Check the Form Behavior

- Select **Additional Accessories** and confirm **Accessories Details** appears and becomes mandatory.
- Select **Reset Form** to clear the form fields.

## Repository Structure

- `Documentation/` — detailed project documents and setup instructions.
- `UpdateSets/` — exported XML update set for deployment.
- `README.md` — project overview and usage guide.

## Documentation

The `Documentation/` folder contains step-by-step instructions for creating the catalog item, screenshots of configuration, explanations of variables, UI Policies, and UI Actions, and deployment instructions for Update Sets.

## Benefits

- **Faster requests:** employees can submit requests through a consistent catalog form.
- **Fewer errors:** dynamic fields collect relevant information when needed.
- **Reusable configuration:** the Update Set can be deployed to other instances.
- **Improved experience:** clear instructions and a reset button make the form easier to use.

## Conclusion

This project demonstrates how the ServiceNow Service Catalog can make routine IT requests more consistent and easier to manage. The Laptop Request Catalog Item helps improve service delivery, employee experience, and the quality of request information.
