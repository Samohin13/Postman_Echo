{
"$schema": "http://json-schema.org/draft-07/schema", // версия схемы: https://json-schema.org/understanding-json-schema/reference/schema.html
"type": "array", // тип корневого элемента: https://json-schema.org/understanding-json-schema/reference/type.html
"items": { // какие элементы допустимы внутри массива: https://json-schema.org/understanding-json-schema/reference/array.html#items
"type": "object", // должны быть объектами: https://json-schema.org/understanding-json-schema/reference/object.html
"required": [ // должны содержать следующие поля: https://json-schema.org/understanding-json-schema/reference/object.html#required-properties
"id",
"name",
"number",
"balance",
"currency"
],
"additionalProperties": false, // дополнительных полей быть не должно
"properties": { // описание полей: https://json-schema.org/understanding-json-schema/reference/object.html#properties
"id": {
"type": "integer" // целое число: https://json-schema.org/understanding-json-schema/reference/numeric.html#integer
},
"name": {
"type": "string", // строка: https://json-schema.org/understanding-json-schema/reference/string.html
"minLength": 1 // минимальная длина - 1: https://json-schema.org/understanding-json-schema/reference/string.html#length
},
"number": {
"type": "string", // строка: https://json-schema.org/understanding-json-schema/reference/string.html
"pattern": "^•• \\d{4}$" // соответствует регулярному выражению: https://json-schema.org/understanding-json-schema/reference/string.html#regular-expressions
},
"balance": {
"type": "integer" // целое число: https://json-schema.org/understanding-json-schema/reference/numeric.html#integer
},
"currency": {
"type": "string" // строка: https://json-schema.org/understanding-json-schema/reference/string.html
}
}
}
}