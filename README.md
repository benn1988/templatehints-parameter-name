# magento2-templatehints
Add the option to customize templatehints parameter name:

By default, if you enable `Stores -> Settings -> All Stores -> Advanced -> Developer -> Debug -> Enable Hints for Storefront with URL Parameter` / `dev/debug/template_hints_storefront_show_with_parameter`, the only option you have for the parameter name, is `templatehints`, because it is hard coded inside `\Magento\Developer\Model\TemplateEngine\Plugin\DebugHints::afterCreate`, there is no option to customize parameter name.

For me, it was annoying during debugging to write so many letters just to enable the hints. 
That is why I have created this module, which is adding the `Stores -> Settings -> All Stores -> Advanced -> Developer -> Debug -> Parameter Name` option in the admin panel. By default, it is set to `h`, but you can of course set it to any value you want. This, on top with changing the default `Parameter Value` from default `magento` to a 1 char value, like `1` or `y` instead, makes activating the hints a lot faster.

`?/h=1` vs `?/templatehints=magento`
