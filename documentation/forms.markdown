# How to render Semantic UI forms
Forms created with the Symfony Form component and Twig templates can be
customized to render as Semantic UI forms using [the form theme][form-theme]
included in this bundle. For more information on using form themes, take a look
at the [Symfony Form documentation][form-themes-docs].

## Render a single form
To render a single form with the Semantic UI form theme, include the
`form_theme` tag inside your template:

```twig
{% extends 'base.html.twig' %}

{% form_theme form '@SemanticUi/form/semantic_2_layout.html.twig' %}

{% block content %}
    {# ... render the form #}

    {{ form(form) }}
{% endblock %}
```

## Render all forms
To render all forms in your application with the Semantic UI form theme, add the
following configuration for the Twig component to your Symfony application:

```yaml
# app/config/config.yml (Symfony 3)
# config/packages/twig.yaml (Symfony 4+)
twig:
    form_themes:
        - '@SemanticUi/form/semantic_2_layout.html.twig'
```

[form-theme]: https://github.com/codedmonkey/semantic-ui-bundle/blob/master/source/Resources/views/form/semantic_2_layout.html.twig
[form-themes-docs]: https://symfony.com/doc/current/form/form_themes.html
