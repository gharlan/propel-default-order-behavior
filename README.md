DefaultOrderBehavior for [Propel2](https://github.com/propelorm/Propel2)
==================================

The Behavior lets you define the default order for tables.

Installation
------------

Add the package to your `composer.json`:

```json
{
    "require": {
        "gharlan/propel-default-order-behavior": "~1.0@dev"
    }
}
```

Usage
-----

```xml
    <table name="default_order_1">
        <column name="id" required="true" primaryKey="true" autoIncrement="true" type="INTEGER" />
        <column name="title" type="VARCHAR" />

        <behavior name="default-order">
            <parameter name="column" value="title"/>
        </behavior>
    </table>

    <table name="default_order_2">
        <column name="id" required="true" primaryKey="true" autoIncrement="true" type="INTEGER" />
        <column name="title" type="VARCHAR" />

        <behavior name="default-order">
            <parameter name="column1" value="title"/>
            <parameter name="column2" value="id desc"/>
        </behavior>
    </table>
```

License
-------

See the [LICENSE](LICENSE) file.
