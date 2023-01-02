---
title: 競プロ精進
---

<table>
    {% for row in site.data.contest %}
        {% if forloop.first %}
        <tr>
            <th>Link</th>
            {% for pair in row %}
                <th>{{ pair[0] }}</th>
            {% endfor %}
        </tr>
        {% endif %}
        <tr>
            <td><a class="external" target="_blank"
                href="{{ site.content.atcoder }}/{{ row["Contest"] | downcase }}/tasks/{{ row["Contest"] | downcase}}_{{ row["Problem"] | downcase }}">link</a></td>
            {% for pair in row %}
                <td>{{ pair[1] }}</td>
            {% endfor %}
        </tr>
    {% endfor %}
</table>
