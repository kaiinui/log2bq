log2bq
======

[AppEngine/Java] Transfer Logs to BigQuery.

```xml
<!-- cron.xml -->
<?xml version="1.0" encoding="UTF-8"?>
<cronentries>
  <cron>
    <url>/_cron/log2bq</url>
    <description>Transfer Logs to BigQuery</description>
    <schedule>every 1 hour</schedule>
  </cron>
</cronentries>
```

```xml
<!-- web.xml -->
<servlet>
    <servlet-name>log2bq</servlet-name>
    <servlet-class>com.kaiinui.log2bq.Log2BqServlet</servlet-class>
</servlet>
<servlet-mapping>
    <servlet-name>log2bq</servlet-name>
    <url-pattern>/_cron/log2bq</url-pattern>
</servlet-mapping>
```
