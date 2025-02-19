---
layout: default
group:  UI Library
subgroup: G_UI definition.xml
title: definition.xml
menu_title: definition.xml
menu_node: parent
version: 2.0
github_link: ui-components/ui-definition.md
redirect_from: /guides/v2.0/ui-library/ui-definition.html

---

<h2 id="example">definition.xml</h2>

{% highlight XML %}
<?xml version="1.0" encoding="UTF-8"?>
<!--
/**
 * Copyright © 2015 Magento. All rights reserved.
 * See COPYING.txt for license details.
 */
-->
<components xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="../../../../etc/ui_definition.xsd">
    <dataSource class="Magento\Ui\Component\DataSource"/>
    <listing sorting="true" class="Magento\Ui\Component\Listing">
        <argument name="data" xsi:type="array">
            <item name="template" xsi:type="string">templates/listing/default</item>
            <item name="save_parameters_in_session" xsi:type="string">1</item>
            <item name="client_root" xsi:type="string">mui/index/render</item>
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">uiComponent</item>
            </item>
        </argument>
    </listing>

    <paging class="Magento\Ui\Component\Paging">
        <argument name="data" xsi:type="array">
            <item name="template" xsi:type="string">templates/paging/default</item>
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/grid/paging</item>
            </item>
        </argument>
    </paging>

    <filters class="Magento\Ui\Component\Filters">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/grid/filters/filters</item>
            </item>
        </argument>
    </filters>
    <filterSearch class="Magento\Ui\Component\Filters\Type\Search">
        <argument name="data" xsi:type="array">
            <item name="config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/grid/search/search</item>
                <item name="displayArea" xsi:type="string">dataGridFilters</item>

            </item>
        </argument>
    </filterSearch>
    <filterSelect class="Magento\Ui\Component\Filters\Type\Select">
        <argument name="data" xsi:type="array">
            <item name="config" xsi:type="array">
                <item name="template" xsi:type="string" translate="true">ui/grid/filters/elements/select</item>
            </item>
        </argument>
    </filterSelect>
    <filterRange class="Magento\Ui\Component\Filters\Type\Range">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/grid/filters/group</item>
            </item>
        </argument>
    </filterRange>
    <filterInput class="Magento\Ui\Component\Filters\Type\Input">
        <argument name="data" xsi:type="array">
            <item name="config" xsi:type="array">
                <item name="template" xsi:type="string">ui/grid/filters/elements/input</item>
            </item>
        </argument>
    </filterInput>
    <filterDate class="Magento\Ui\Component\Filters\Type\Date">
        <argument name="data" xsi:type="array">
            <item name="config" xsi:type="array">
                <item name="template" xsi:type="string">ui/grid/filters/elements/date</item>
            </item>
        </argument>
    </filterDate>
    <container class="Magento\Ui\Component\Container">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">uiComponent</item>
            </item>
            <item name="template" xsi:type="string">templates/container/default</item>
        </argument>
    </container>
    <massaction class="Magento\Ui\Component\MassAction">
        <argument name="data" xsi:type="array">
            <item name="template" xsi:type="string">templates/listingcontainer/massaction/default</item>
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/grid/massactions</item>
            </item>
        </argument>
    </massaction>
    <actions class="Magento\Ui\Component\Control\Action">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/grid/columns/actions</item>
            </item>
        </argument>
    </actions>




    <columns class="Magento\Ui\Component\Listing\Columns">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/grid/listing</item>
            </item>
        </argument>
    </columns>
    <column class="Magento\Ui\Component\Listing\Columns\Column">
        <argument name="data" xsi:type="array">
            <item name="state_prefix" xsi:type="string">columns</item>
        </argument>
    </column>


    <form class="Magento\Ui\Component\Form">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/form</item>
            </item>
            <item name="template" xsi:type="string">templates/form/default</item>
        </argument>
    </form>
    <fieldset class="Magento\Ui\Component\Form\Fieldset">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/components/fieldset</item>
            </item>
        </argument>
    </fieldset>
    <field class="Magento\Ui\Component\Form\Field"/>

    <!-- Form elements -->
    <input class="Magento\Ui\Component\Form\Element\Input">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/element/abstract</item>
                <item name="config" xsi:type="array">
                    <item name="template" xsi:type="string">ui/form/field</item>
                    <item name="elementTmpl" xsi:type="string">ui/form/element/input</item>
                </item>
            </item>
        </argument>
    </input>
    <checkbox class="Magento\Ui\Component\Form\Element\Checkbox">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/element/boolean</item>
                <item name="config" xsi:type="array">
                    <item name="template" xsi:type="string">ui/form/field</item>
                    <item name="elementTmpl" xsi:type="string">ui/form/element/checkbox</item>
                </item>
            </item>
        </argument>
    </checkbox>
    <select class="Magento\Ui\Component\Form\Element\Select">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/element/select</item>
                <item name="config" xsi:type="array">
                    <item name="template" xsi:type="string">ui/form/field</item>
                    <item name="elementTmpl" xsi:type="string">ui/form/element/select</item>
                </item>
            </item>
        </argument>
    </select>
    <multiselect class="Magento\Ui\Component\Form\Element\Select">
        <argument name="data" xsi:type="array">
            <item name="template" xsi:type="string">ui/form/element/multiselect</item>
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/element/multiselect</item>
                <item name="config" xsi:type="array">
                    <item name="template" xsi:type="string">ui/form/field</item>
                    <item name="elementTmpl" xsi:type="string">ui/form/element/multiselect</item>
                </item>
            </item>
        </argument>
    </multiselect>
    <textarea class="Magento\Ui\Component\Form\Element\Textarea">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/element/textarea</item>
                <item name="config" xsi:type="array">
                    <item name="template" xsi:type="string">ui/form/field</item>
                    <item name="elementTmpl" xsi:type="string">ui/form/element/textarea</item>
                </item>
            </item>
        </argument>
    </textarea>
    <multiline class="Magento\Ui\Component\Form\Element\Multiline">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/components/group</item>
            </item>
        </argument>
    </multiline>
    <!-- Form elements -->

    <!-- Form element data types -->
    <text class="Magento\Ui\Component\Form\Element\DataType\Text">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/element/text</item>
            </item>
        </argument>
    </text>
    <number class="Magento\Ui\Component\Form\Element\DataType\Number"/>
    <price class="Magento\Ui\Component\Form\Element\DataType\Price"/>
    <image class="Magento\Ui\Component\Form\Element\DataType\Media">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/element/abstract</item>
                <item name="config" xsi:type="array">
                    <item name="template" xsi:type="string">ui/form/field</item>
                    <item name="elementTmpl" xsi:type="string">ui/form/element/media</item>
                </item>
            </item>
        </argument>
    </image>
    <date class="Magento\Ui\Component\Form\Element\DataType\Date">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/element/date</item>
                <item name="config" xsi:type="array">
                    <item name="template" xsi:type="string">ui/form/field</item>
                    <item name="elementTmpl" xsi:type="string">ui/form/element/date</item>
                </item>
            </item>
        </argument>
    </date>
    <boolean class="Magento\Ui\Component\Form\Element\DataType\Boolean">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/element/abstract</item>
                <item name="config" xsi:type="array">
                    <item name="template" xsi:type="string">ui/form/field</item>
                    <item name="elementTmpl" xsi:type="string">ui/form/element/input</item>
                </item>
            </item>
        </argument>
    </boolean>
    <email class="Magento\Ui\Component\Form\Element\DataType\Email">
        <argument name="data" xsi:type="array">
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/element/abstract</item>
                <item name="config" xsi:type="array">
                    <item name="template" xsi:type="string">ui/form/field</item>
                    <item name="elementTmpl" xsi:type="string">ui/form/element/email</item>
                </item>
            </item>
            <item name="config" xsi:type="array">
                <item name="addbefore" xsi:type="string">@email:</item>
            </item>
        </argument>
    </email>
    <!-- Form element data types -->


    <tab class="Magento\Ui\Component\Layout\Tabs\Tab">
        <argument name="data" xsi:type="array">
            <item name="template" xsi:type="string">templates/layout/tabs/tab/default</item>
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/components/area</item>
            </item>
        </argument>
    </tab>
    <!-- navigation -->
    <nav class="Magento\Ui\Component\Layout\Tabs\Nav">
        <argument name="data" xsi:type="array">
            <item name="template" xsi:type="string">ui/tab</item>
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/form/components/tab_group</item>
            </item>
        </argument>
    </nav>
    <!-- bookmark -->
    <bookmark class="Magento\Ui\Component\Bookmark">
        <argument name="data" xsi:type="array">
        </argument>
    </bookmark>
    <exportButton class="Magento\Ui\Component\ExportButton">
        <argument name="data" xsi:type="array">
            <item name="template" xsi:type="string">templates/export/button</item>
            <item name="js_config" xsi:type="array">
                <item name="component" xsi:type="string">Magento_Ui/js/grid/export</item>
            </item>
            <item name="config" xsi:type="array">
                <item name="displayArea" xsi:type="string">dataGridActions</item>
                <item name="options" xsi:type="array">
                    <item name="cvs" xsi:type="array">
                        <item name="value" xsi:type="string">csv</item>
                        <item name="label" xsi:type="string" translate="true">CSV</item>
                        <item name="url" xsi:type="string">mui/export/gridToCsv</item>
                    </item>
                    <item name="xml" xsi:type="array">
                        <item name="value" xsi:type="string">xml</item>
                        <item name="label" xsi:type="string" translate="true">Excel XML</item>
                        <item name="url" xsi:type="string">mui/export/gridToXml</item>
                    </item>
                </item>
            </item>
        </argument>
    </exportButton>
</components>
{% endhighlight %}   
