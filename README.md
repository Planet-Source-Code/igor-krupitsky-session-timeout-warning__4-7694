<div align="center">

## Session Timeout Warning


</div>

### Description

Warn users about Session Timeout 5 minutes before it happens.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Igor Krupitsky](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/igor-krupitsky.md)
**Level**          |Beginner
**User Rating**    |4.7 (28 globes from 6 users)
**Compatibility**  |ASP \(Active Server Pages\), HTML
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__4-1.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/igor-krupitsky-session-timeout-warning__4-7694/archive/master.zip)





### Source Code

```
<html>
<head>
<script language="javascript">
function WarnUserTimeout()
{
	if (window.confirm('Your session will expire in 5 minutes. Do you want to continue working?'))
	{
		window.history.go(0)
	}
}
</script>
</head>
<body OnLoad="window.setTimeout('WarnUserTimeout()',(<%=session.timeout%>-5)*60*1000)">
Some Text...
</body>
</html>
```

