{
    "name": "Connect Wazzup by @shorin_nikita",
    "flow": [
        {
            "id": 1,
            "module": "http:ActionSendData",
            "version": 3,
            "parameters": {
                "handleErrors": true,
                "useNewZLibDeCompress": true
            },
            "filter": {
                "name": "AIBot.School",
                "conditions": []
            },
            "mapper": {
                "ca": "",
                "qs": [],
                "url": "https://api.wazzup24.com/v3/webhooks",
                "data": "{\n  \"webhooksUri\": \"{{var.input.webhook_url}}\",\n  \"subscriptions\": {\n    \"messagesAndStatuses\": true\n  }\n}",
                "gzip": true,
                "method": "patch",
                "headers": [
                    {
                        "name": "Authorization",
                        "value": "Bearer {{var.input.wazzup_api_key}}"
                    }
                ],
                "timeout": "",
                "useMtls": false,
                "authPass": "",
                "authUser": "",
                "bodyType": "raw",
                "contentType": "application/json",
                "serializeUrl": false,
                "shareCookies": false,
                "parseResponse": false,
                "followRedirect": true,
                "useQuerystring": false,
                "followAllRedirects": false,
                "rejectUnauthorized": true
            },
            "metadata": {
                "designer": {
                    "x": 0,
                    "y": 0
                },
                "restore": {
                    "expect": {
                        "qs": {
                            "mode": "chose"
                        },
                        "method": {
                            "mode": "chose",
                            "label": "PATCH"
                        },
                        "headers": {
                            "mode": "chose",
                            "items": [
                                null
                            ]
                        },
                        "bodyType": {
                            "label": "Raw"
                        },
                        "contentType": {
                            "label": "JSON (application/json)"
                        }
                    }
                },
                "parameters": [
                    {
                        "name": "handleErrors",
                        "type": "boolean",
                        "label": "Evaluate all states as errors (except for 2xx and 3xx )",
                        "required": true
                    },
                    {
                        "name": "useNewZLibDeCompress",
                        "type": "hidden"
                    }
                ],
                "expect": [
                    {
                        "name": "url",
                        "type": "url",
                        "label": "URL",
                        "required": true
                    },
                    {
                        "name": "serializeUrl",
                        "type": "boolean",
                        "label": "Serialize URL",
                        "required": true
                    },
                    {
                        "name": "method",
                        "type": "select",
                        "label": "Method",
                        "required": true,
                        "validate": {
                            "enum": [
                                "get",
                                "head",
                                "post",
                                "put",
                                "patch",
                                "delete",
                                "options"
                            ]
                        }
                    },
                    {
                        "name": "headers",
                        "spec": [
                            {
                                "name": "name",
                                "type": "text",
                                "label": "Name",
                                "required": true
                            },
                            {
                                "name": "value",
                                "type": "text",
                                "label": "Value"
                            }
                        ],
                        "type": "array",
                        "label": "Headers"
                    },
                    {
                        "name": "qs",
                        "spec": [
                            {
                                "name": "name",
                                "type": "text",
                                "label": "Name",
                                "required": true
                            },
                            {
                                "name": "value",
                                "type": "text",
                                "label": "Value"
                            }
                        ],
                        "type": "array",
                        "label": "Query String"
                    },
                    {
                        "name": "bodyType",
                        "type": "select",
                        "label": "Body type",
                        "validate": {
                            "enum": [
                                "raw",
                                "x_www_form_urlencoded",
                                "multipart_form_data"
                            ]
                        }
                    },
                    {
                        "name": "parseResponse",
                        "type": "boolean",
                        "label": "Parse response",
                        "required": true
                    },
                    {
                        "name": "authUser",
                        "type": "text",
                        "label": "User name"
                    },
                    {
                        "name": "authPass",
                        "type": "password",
                        "label": "Password"
                    },
                    {
                        "name": "timeout",
                        "type": "uinteger",
                        "label": "Timeout",
                        "validate": {
                            "max": 300,
                            "min": 1
                        }
                    },
                    {
                        "name": "shareCookies",
                        "type": "boolean",
                        "label": "Share cookies with other HTTP modules",
                        "required": true
                    },
                    {
                        "name": "ca",
                        "type": "cert",
                        "label": "Self-signed certificate"
                    },
                    {
                        "name": "rejectUnauthorized",
                        "type": "boolean",
                        "label": "Reject connections that are using unverified (self-signed) certificates",
                        "required": true
                    },
                    {
                        "name": "followRedirect",
                        "type": "boolean",
                        "label": "Follow redirect",
                        "required": true
                    },
                    {
                        "name": "useQuerystring",
                        "type": "boolean",
                        "label": "Disable serialization of multiple same query string keys as arrays",
                        "required": true
                    },
                    {
                        "name": "gzip",
                        "type": "boolean",
                        "label": "Request compressed content",
                        "required": true
                    },
                    {
                        "name": "useMtls",
                        "type": "boolean",
                        "label": "Use Mutual TLS",
                        "required": true
                    },
                    {
                        "name": "contentType",
                        "type": "select",
                        "label": "Content type",
                        "validate": {
                            "enum": [
                                "text/plain",
                                "application/json",
                                "application/xml",
                                "text/xml",
                                "text/html",
                                "custom"
                            ]
                        }
                    },
                    {
                        "name": "data",
                        "type": "buffer",
                        "label": "Request content"
                    },
                    {
                        "name": "followAllRedirects",
                        "type": "boolean",
                        "label": "Follow all redirect",
                        "required": true
                    }
                ]
            }
        }
    ],
    "metadata": {
        "instant": false,
        "version": 1,
        "scenario": {
            "roundtrips": 1,
            "maxErrors": 3,
            "autoCommit": true,
            "autoCommitTriggerLast": true,
            "sequential": false,
            "slots": null,
            "confidential": false,
            "dataloss": false,
            "dlq": false,
            "freshVariables": false
        },
        "designer": {
            "orphans": []
        },
        "zone": "eu2.make.com",
        "notes": [
            {
                "moduleIds": [
                    1
                ],
                "content": "<p><strong>PrideAIBot</strong> by <a href=\"https://www.youtube.com/@shorin_nikita\" target=\"_blank\">shorin_nikita</a></p>",
                "isFilterNote": false,
                "metadata": {
                    "color": "#9138FE"
                }
            }
        ]
    },
    "io": {
        "input_spec": [
            {
                "name": "wazzup_api_key",
                "type": "text",
                "label": "",
                "default": "ЗАМЕНИТЬ",
                "required": false,
                "multiline": false
            },
            {
                "name": "webhook_url",
                "type": "text",
                "label": "",
                "default": "ЗАМЕНИТЬ",
                "required": false,
                "multiline": false
            }
        ],
        "output_spec": []
    }
}
