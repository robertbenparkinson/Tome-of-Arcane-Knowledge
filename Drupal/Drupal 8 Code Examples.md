# Drupal 8 Code Examples

## Attach an existing webform to a custom twig template

### Controller

```php
namespace Drupal\gorn\Controller;

use Drupal\Core\Controller\ControllerBase;
use Drupal\webform;

class GornController extends ControllerBase {

  public function gorn_page() {

      $build['#theme'] = 'gorn_page';

      $my_webform_machinename = 'gorn_webform';
      $my_form = \Drupal\webform\Entity\Webform::load($my_webform_machinename);
      $build['#gorn_webform'] = \Drupal::entityTypeManager()->getViewBuilder('webform')->view($my_form);

      return $build;
  }

}
```

### Module/Hook

```php
use Drupal\Core\Routing\RouteMatchInterface;

function gorn_theme() {
  return [
    'gorn_page' => [
        'variables' => [
            'title' => NULL,
            'gorn_webform' => NULL,
        ],
    ],
  ];
}
```

### TWIG gorn-page.html.twig

```html
{{ gorn_webform }}
```