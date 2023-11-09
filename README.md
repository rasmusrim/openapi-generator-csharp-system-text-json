# CSharp generator using System.Text.Json

I have made a fork of the csharp generator using System.Text.Json instead of Newtonsoft.

Clone it, and then run your openapi-generator-cli command as normal, but add a -t with the path to the cloned directory. I would do something like this:

    npx @openapitools/openapi-generator-cli generate -i http://localhost:5166/swagger/v1/swagger.json -g csharp -o Api.ClientSdk --library httpclient --additional-properties=packageName=Flyttavle.Plugins.PortFlowPlugin,nullableReferenceTypes=true,useDateTimeOffset=true -t ~/source/repos/openapi-generator-csharp-systen-text-json

It is only tested on one of my codebases. Please raise an issue and submit a swagger file if you find some problems.

