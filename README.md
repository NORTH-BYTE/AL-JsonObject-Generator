# AL JsonObject Generator

AL JsonObject Generator is a lightweight productivity extension for AL developers working with Business Central and JSON integrations.

The extension helps you automatically generate `JsonObject.Add(...)` mappings based on predefined field mappings (such as Item, Customer, and Vendor).  
It can also generate a full AL procedure for you, making integration work significantly faster and less error-prone.

---

## ✨ Features

### 🔧 QuickFix triggered by `BuildJson`
Write **`BuildJson`** (or `buildjson`) on a new line in any AL file and press **`Ctrl + .`**.

You will be prompted to:

1. **Select a standard Business Central table**  
   (e.g., Item, Customer, Vendor)

2. **Choose the output mode:**
   - Generate a **full AL procedure**, or
   - Generate **only the `JsonObject.Add(...)` lines**

#### Example: Full procedure generation
```al
procedure BuildJsonObjectItem()
var
    JsonObject: JsonObject;
    Item: Record Item;
begin
    JsonObject.Add('No.', Item."No.");
    JsonObject.Add('Description', Item."Description");
    JsonObject.Add('Unit Price', Item."Unit Price");

    // ...
end;
