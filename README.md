# Apex Search LOV From Query

A lightweight, reusable searchable LOV component for Oracle APEX, built from scratch using PL/SQL, JavaScript, and CSS.

## Why this component?

Oracle APEX provides built-in LOV page items such as **Select List from Query**, but they cannot be embedded directly inside an Interactive Report with built-in search functionality.

This component fills that gap by providing a reusable PL/SQL function that creates a searchable dropdown inside an Interactive Report from any SQL query.

The function displays a **Display Value** to the user while returning the corresponding **Return Value**, matching the behavior of Oracle APEX LOV items.

## Features

* Adds a searchable LOV to Interactive Reports.
* Accepts any SQL query as the data source.
* Displays a Display Value while returning a Return Value.
* Search while typing.
* Automatic HTML generation using PL/SQL.
* Built-in JavaScript and CSS behavior.
* No external Oracle APEX plug-ins required.
* Lightweight and reusable.

## Demo

![Demo](video.gif)

## Usage

```sql
SELECT
    employee_name,
    Ax_lov_query(
        department_id,
        q'[
            SELECT department_id,
                   department_name
            FROM departments
            ORDER BY department_name
        ]'
    ) AS department
FROM employees;
```

## License

MIT License
