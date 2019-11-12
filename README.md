# xaml-hot-reload-workaround

## Workaround when using Xamarin.Forms XAML Hot Reload with base templates

XAML Hot Reload currently uses very broad techniques for reloading XAML pages. If you include a base `ContentPage`, your changes may not be reflected since, if you have in-constructor scafolding, they will be not be recreated.

There is a workaround for this: By putting your scafolding of your base page in `InitializeComponent`, you should be fired when changes to your XAML occure.

**NOTE:**

This does not apply to code-behind changes, if you modify the cs template, you will need to reload your application fully for it to be reflected.
