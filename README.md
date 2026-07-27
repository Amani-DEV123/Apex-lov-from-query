# Apex-lov-from-query

Apex Search LOV From Query is a lightweight searchable LOV component for Oracle APEX.

It allows you to generate a reusable search-enabled LOV directly from SQL using the `get_search_lov` function, without requiring any APEX plug-ins.

## Features

- Search while typing
- Pure SQL function
- No plugin required
- Lightweight
- Works in Interactive Report
- Reusable

## Demo

![Demo](video.gif)

## Usage

```sql
SELECT
    employee_name,
    Apex_lov_query(
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
