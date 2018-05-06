A curated and organized collection of functional odoo patches. ("Good bye [OCB](https://github.com/oca/ocb)")

# Naming Convention

For this to work as intended, we rely on the follonwing naming convention:

### Regex in pcre (php) flavor

[Regex101 Playground](https://regex101.com/r/kv21jD/2)

```regex
(?'id'\d\d\d\d)-(?:(?'deps'\[(?:\d\d\d\d,)*(?:\d\d\d\d)\])-|)(?'scope'list|of|odoo|modules|please insert the whole list)::(?'desc'.*)\.patch
```

### Examples
```bash
0001-odoo::This-should-be-a-really-long-and-comprehensive-naming-of-the-patch-to-save-on-OP-hoops.patch
0002-[0001]-odoo::This-patch-depends-on-0001-expressed-by-the-[0001]-before-the-module.patch
0003-hr_payroll::Oh-and-the-odoo-module-represents-a-global-scoped-patch-which-spans-more-than-one-module.patch
0004-[0003]-hr_payroll_account::This-might-be-a-sister-patch-which-only-can-be-ab=pplied-if-the-module-will-be-installed.patch
```

# Instructions
 ```patch
 This may be some useful description of this patch that
 will be ignored by the diff/patch utility. USE IT!

 --- a/foo  2002-02-21 23:30:39.942229878 -0800
 +++ b/foo  2002-02-21 23:30:50.442260588 -0800
 @@ -1,7 +1,6 @@
 -The Way that can be told of is not the eternal Way;
 -The name that can be named is not the eternal name.
  The Nameless is the origin of Heaven and Earth;
 -The Named is the mother of all things.
 +The named is the mother of all things.
 +
 ```

# Credits & License

Base on stewardship by:
 - [@yelizariev](https://github.com/yelizariev) ([IT-Projects LLC](https://it-projects.info))
 - [@blaggacao](https://github.com/blaggacao) ([XOE Solutions](https://xoe.solutions))

License: [LGPL-3](https://www.gnu.org/licenses/lgpl-3.0.en.html)