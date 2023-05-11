```mermaid
erDiagram

Question ||--o{ Answer: "1:多"
Birthplace ||--o{ Staff: "1:多"
Question ||--|| Staff: "1:1"
Answer ||--|| Staff: "1:1"

Question{
INT id(PK)
INT staff_id(FK)
TEXT content
DATE day
VARCHAR(13) name
VARCHAR(20) delete_id
VARCHAR(7) icon
}

Answer{
INT id(PK)
INT staff_id(FK)
TEXT content
DATE day
VARCHAR(13) name
VARCHAR(20) delete_id
VARCHAR(7) icon
INT question
}

Staff{
 INT id(PK)
 VARCHAR(5) staff_name
 VARCHAR(30) picture
 INT birthplace_id(FK)
 TEXT yarakashi
 TEXT dream
 VARCHAR(15) passwd
 CHAR del_flg
 DATETIME created_on
 VARCHAR(5) created_by
 DATETIME updated_on
 VARCHAR(5) update_by
}

Birthplace{
INT id(PK)
VARCHAR(3) birthplace_name
}

.mermaid {
  max-width: 100%;
  height:  ;
}
```
