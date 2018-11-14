---
layout: post
title:  "My second post!"
date:   2018-11-14 16:28:18 +0100
categories: jekyll update
---
This is my second post and I still don't know what can I do with it


<html>
<head>
    <title>JSSample</title>
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.0/jquery.min.js"></script>
</head>
<body>

<script type="text/javascript">
    $(function() {
        var params = {
            // Request parameters
            "startDate": "{string}",
        };
      
        $.ajax({
            url: "https://azwussnbapi01p.azure-api.net/ls-api/openapi/centers/{centerId}/schedule?" + $.param(params),
            beforeSend: function(xhrObj){
                // Request headers
                xhrObj.setRequestHeader("Ocp-Apim-Subscription-Key","{subscription key}");
            },
            type: "GET",
            // Request body
            data: "{body}",
        })
        .done(function(data) {
            alert("success");
        })
        .fail(function() {
            alert("error");
        });
    });
</script>
</body>
</html>