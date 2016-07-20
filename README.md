# tpa-i18n

Component used to provide generic Behavior for adding web analytics to your component. It will fire generic events, to
which applications may decide to attach monitoring by configuring a specific component (e.g. for Google Analytics and/or
Webtrekk).

## Example

To use the behavior, you need to add this behavior to your web component. 
 
```
 <link rel="import" href="../tpa-web-analytics.html">

    <dom-module id="my-component">
        <template>...</template>
        <script>

            Polymer({
                is:"my-component",
                behaviors: [WebAnalyticsBehavior],

                properties: {
                },

                awesomeFunction: function() {
                    //do some awesome stuff
                    //and notify that you just did some awesome stuff
                    this.webAnalyticsActionEvent('just did some awesome stuff');
                }
        </script>
    </dom-module>
```


You will then need to make sure your SPA contains at least one web component for actually submitting the gathered
analytics, for example:

```
<tpa-webtrekk></tpa-webtrekk>
```


