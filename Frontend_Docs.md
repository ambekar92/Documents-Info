# Form Fields Documentation

## ComboboxField

The `ComboboxField` component is used for dropdown selections with dynamic data fetching.

### Example Usage:
```jsx
<ComboboxField
  label="Tech Focal Point"
  placeholder=""
  data={getTechnicalUserList}
  id="rfxTechFocalPersonId"
  name="rfxTechFocalPersonId"
  code="rfxTechFocalPersonIdCode"
  description="rfxTechFocalPersonIdDesc"
  iconClassName="dropdownIcon"
  setValue={formInputs.rfxTechFocalPersonId || ""}
  getvalue={setDropdownData}
/>
```

### State Management:
```jsx
const [getDropdownData, setDropdownData] = useState([]);

useEffect(() => {
  if (getDropdownData?.textField === "category") {
    setFormInputs((formInputs) => ({
      ...formInputs,
      [getDropdownData?.textField]: getDropdownData?.name,
    }));
  } else {
    setFormInputs((formInputs) => ({
      ...formInputs,
      [getDropdownData?.textField]: getDropdownData?.selected,
    }));
  }
}, [getDropdownData]);
```

---

## InputField

The `InputField` component is used for text or date inputs.

### Example Usage:
```jsx
<InputField
  id="documentDate"
  className="inputBox"
  label="Document Date"
  name="documentDate"
  placeholder=""
  type="date"
  value={formInputs.documentDate}
  onChange={onInputChange}
  disabled={getDisabledStatus}
/>
```

---

## MultiselectField

The `MultiselectField` component allows selection of multiple options.

### Example Usage:
```jsx
<MultiselectField
  label="Roles"
  placeholder="Please select the Roles"
  data={getRoleIdVal}
  id="roles"
  iconClassName="dropdownIcon"
  name="roles"
  getvalue={setDropdownData}
  className="dropdownOption"
  disabled={true}
  setValue={getRoleIdText}
/>
```

This field is disabled by default but can be enabled based on conditions.
