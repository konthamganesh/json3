def props = readJSON file: 'dir/input.json'
assert props['attr1'] == 'One'
assert props.attr1 == 'One'

def props = readJSON text: '{ "key": "value" }'
assert props['key'] == 'value'
assert props.key == 'value'

def props = readJSON text: '[ "a", "b"]'
assert props[0] == 'a'
assert props[1] == 'b'

def props = readJSON text: '{ "key": null, "a": "b" }', returnPojo: true
assert props['key'] == null
props.each { key, value ->
    echo "Walked through key $key and value $value"
}
