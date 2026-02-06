name: 🚀 Declaration Management Request
description: Add, Update, or Delete entries in the Declaration Table using a simple form.
title: "Declaration: [Country Name]"
labels: ["migration-request"]
body:
  - type: dropdown
    id: action
    attributes:
      label: What action do you want to take?
      options:
        - Add New Key
        - Update Existing Key
        - Delete Key
    validations:
      required: true

  - type: input
    id: country
    attributes:
      label: Country Code
      placeholder: "e.g., ES, UK, FR"
    validations:
      required: true

  - type: input
    id: message_type
    attributes:
      label: Message Type
      placeholder: "e.g., CC415A"
    validations:
      required: true

  - type: textarea
    id: new_values
    attributes:
      label: New Values (For Add or Update)
      description: Enter the new Name, Group, or Dates if applicable.
      placeholder: "MessageName: Standard declaration\nProcedureGroup: Standard"
