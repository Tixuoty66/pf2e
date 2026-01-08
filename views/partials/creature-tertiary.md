**{{'Common.Speed'|l}}** {% if data.movement.walk %}{{data.movement.walk}} feet,{% endif %}{% if data.movement.burrow %} {{'Movement.Burrow'|l|lowercase}} {{data.movement.burrow}} feet,{% endif %}{% if data.movement.climb %} {{'Movement.Climb'|l|lowercase}} {{data.movement.climb}} feet,{% endif %}{% if data.movement.fly %} {{'Movement.Fly'|l|lowercase}} {{data.movement.fly}} feet,{% endif %}{% if data.movement.swim %} {{'Movement.Swim'|l|lowercase}} {{data.movement.swim}} feet{% endif %}{% if data.movement.other %}; {{data.movement.other}}{% endif %}

{% for ability in data.attacks %}
{% include "attack.md" %}
{% endfor %}

{% for spellcasting in data.spellcasting %}
{% include "spellcasting.md" spellcasting %}
{% endfor %}

{% if data.rituals.type %}**{{data.rituals.type}}** {% endif %}{% if data.rituals %}**{{'Creature.Rituals'|l}}** {% if data.rituals.dc %}{{'Common.DC'|l}} {{data.rituals.dc}}; {% endif %}{{data.rituals.text}}{% endif %}

{% for ability in data.abilities.offensive %}
{% include "ability.md" %}
{% endfor %}
