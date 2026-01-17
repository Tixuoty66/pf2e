{% if data.attributes %}
##### {{'Class.KeyAttribute'|l}}

**{{data.attributes|map: "Attribute", " or "}}**

{{'Class.KeyAttributeText'|l}} {{data.attributes|map: 'Attribute', " or "}}.
{% endif %}
---
{% if data.hp %}
##### {{'Common.HitPoints'|l}}

**{{data.hp}} {{'Class.HpText1'|l}}**

{{'Class.HpText2'|l}}
{% endif %}
