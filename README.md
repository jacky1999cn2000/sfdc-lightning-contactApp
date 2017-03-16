# sfdc-lightning-contactApp

* domain: jz-contactapp-dev-ed.my.salesforce.com
* username: jz.lightning.01@jz.com
* password: ba76acaH
* token: TOJuM2nB3uw4FtDOmVfWk6Jet
* tutorial: https://developer.salesforce.com/docs/atlas.en-us.lightning.meta/lightning/events_one_demo.htm


* [.THIS.class vs .THIS .class](https://developer.salesforce.com/docs/atlas.en-us.lightning.meta/lightning/components_css.htm)
```
<div class="slds-grid">
  <div class="slds-col">
    <ui:button label="View Cases" press="{!c.relatedList}" class="btn"/>
  </div>
  <div class="slds-col">
    <ui:button label="View Cases" press="{!c.relatedList}" class="btn"/>
  </div>
</div>

// without space, the rule is for top-level element (elements wrapped by body tag and not by other tags)
/*.THIS.btn {
    width: 100%;
}*/

// with space, the rule is for descendant (not top-level elements)
.THIS .btn {
    width: 100%;
}
```

* [unbound attribute pass](https://developer.salesforce.com/docs/atlas.en-us.lightning.meta/lightning/components_composition.htm)
```
<!--c:nestedComponents2-->
<aura:component>
    <aura:attribute name="passthrough" type="String" default="passed attribute"/>
    Observe!  Components within components!

    <c:helloHTML/>

    <c:helloAttributes whom="{#v.passthrough}"/>
</aura:component>
```
