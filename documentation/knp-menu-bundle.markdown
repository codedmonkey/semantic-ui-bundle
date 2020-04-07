# How to render Semantic UI menus
Menus created with KnpMenuBundle and Twig templates can be customized to render
as Semantic UI menus using [the menu template][menu-template] included in this
bundle. For more information on KnpMenuBundle, take a loot at
[the official documentation][knp-menu-bundle].

## Render a single menu
To render a single menu with the Semantic UI menu theme, add the `template`
parameter in the `knp_menu_render` call:

```twig
{{ knp_menu_render('AppBundle:Builder:mainMenu', {'template': '@SemanticUi/menu/semantic_2_menu.html.twig'}) }}
```

## Render all menus
To render all menus in your application with the Semantic UI menu template, add
the following configuration for KnpMenuBundle to your Symfony application:

```yaml
# app/config/config.yml (Symfony 3)
knp_menu:
    twig:
        template: '@SemanticUi/menu/semantic_2_menu.html.twig'
```
# Add CSS classes to the menu
When using this bundle's menu template, CSS classes can simply be added to the
menu using the built-in features of KnpMenuBundle, the `ui` and `menu` classes
will automatically be wrapped around your classes.

# Render menu items only
Because the purpose of the KnpMenu component is to create only hierarchical
menus, this bundle includes a way to render a menu without it's enclosing
HTML-tag by using the `bare` option. This allows for greater customization when
creating a menu.

```twig
<div class="ui menu">
  {{ knp_menu_render('AppBundle:Builder:primaryMenu', {'template': '@SemanticUi/menu/semantic_2_menu.html.twig', 'bare': true}) }}
  <div class="right menu">
    {{ knp_menu_render('AppBundle:Builder:secondaryMenu', {'template': '@SemanticUi/menu/semantic_2_menu.html.twig', 'bare': true}) }}
  </div>
</div>
```

[knp-menu-bundle]: https://symfony.com/doc/master/bundles/KnpMenuBundle/index.html
[menu-template]: https://github.com/codedmonkey/semantic-ui-bundle/blob/master/source/Resources/views/menu/semantic_2_menu.html.twig
