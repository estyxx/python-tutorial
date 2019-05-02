# Named Tuples

When you need to represent a list of identical objects with different values, you start with a list of tuples. It’s an efficient way to hold a collection of related data. Tuples are like structures or records in other languages, but indexed with integers, like lists. You can build a list named people, where each element is a tuple of three elements: first name, last name, and zip code. To get the zip code for the first element, you can use people[0][2].

The problem comes when you want to read in a file where each line has 17 fields. It gets really hard to remember which index is for which field. At this point, many programmers create a class with read-only properties for this purpose, so they can say class.field (e.g., people[0].first_name, people[0].last_name, etc.). Such a class has no methods; it only exists to store the data.

It’s overkill to use a class for this purpose. Python provides an elegant solution – named tuples. A named tuple is exactly like a normal tuple, except that the fields can also be accessed by .fieldname. Named tuples are still immutable, you can still index elements with integers, and you can iterate over the elements. With a named tuple, you can say record.first_name, record.last_name, as with a class, but without the extra code of a class. There’s no need to write all the property definitions.

The `collections.namedtuple` function is a factory that produces subclasses of tuple
enhanced with field names and a class name — which helps debugging.

NOTE: *Instances of a class that you build with namedtuple take exactly the
same amount of memory as tuples because the field names are stor‐
ed in the class. They use less memory than a regular object because
they do store attributes in a per-instance `__dict__`*

## Defining and using a named tuple type

```python
>>> from collections import namedtuple
>>> City = namedtuple('City', 'name country population coordinates') (1)
>>> tokyo = City('Tokyo', 'JP', 36.933, (35.689722, 139.691667)) (2)
tokyo
>>> City(name='Tokyo', country='JP', population=36.933, coordinates=(35.689722, 139.691667))
>>> tokyo.population (3)
36.933
>>> tokyo.coordinates
(35.689722, 139.691667)
>>> tokyo[1]
'JP'
```

- (1) Two parameters are required to create a named tuple: a class name and a list of
field names, which can be given as an iterable of strings or as a single spacedelimited string 
- (2) Data must be passed as positional arguments to the constructor (in contrast, the
tuple constructor takes a single iterable).
- (3) You can access the fields by name or position.

## Named tuple attributes and methods

A named tuple type has a few attributes in addition to those inherited from tuple.
The following code shows the most useful: the _fields class attribute, the class method
`_make(iterable)` and the `_asdict()` instance method

```python
>>> City._fields (1)
('name', 'country', 'population', 'coordinates')
>>> LatLong = namedtuple('LatLong', 'lat long')
>>> delhi_data = ('Delhi NCR', 'IN', 21.935, LatLong(28.613889, 77.208889))
>>> delhi = City._make(delhi_data) (2)
>>> delhi._asdict() (3)
OrderedDict([('name', 'Delhi NCR'), ('country', 'IN'), ('population',
21.935), ('coordinates', LatLong(lat=28.613889, long=77.208889))])
>>> for key, value in delhi._asdict().items():
        print(key + ':', value)
name: Delhi NCR
country: IN
population: 21.935
coordinates: LatLong(lat=28.613889, long=77.208889)
```

- (1) `_fields` is a tuple with the field names of the class.
- (2) `_make()` lets you instantiate a named tuple from an iterable; City(*delhi_da
ta) would do the same.
- (3) `_asdict()` returns a collections.OrderedDict built from the named tuple
instance. That can be used to produce a nice display of city data.

[Previous](exceptions.md) | [Next](datatypes.md) |
[List of contents](../README.md#basics)