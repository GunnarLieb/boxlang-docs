[comment]: # (Note: This documentation is generated dynamically in the build process.  To modify the contents, change the javadoc on the _invoke method of the BIF class)

# Function: `GetBoxCacheFilter`

This method creates a cache filter that can be used to operate on a cache instance and its keys.

The filter can be used to clear, get, or remove keys from the cache.

 All filters must be adhere to the ,{@link ICacheKeyFilter}, interface.

 Example:

 ,<pre>,
 getBoxCache().clear( getBoxCacheFilter( "foo*" ) );
 getBoxCache().clear( getBoxCacheFilter( ".*foo.*", true ) );

 You can also create your own custom cache filter by using a closure/lambda that
 accepts a ,{@code
 Key
 }, and returns a boolean.

 Example:

 ,<pre>,
 getBoxCache().clear( key -> key.getName().startsWith( "foo" ) );
 getBoxCache().clear( key -> key.getName().matches( ".*foo.*" ) );
 ,</pre>

## Method Signature

```
GetBoxCacheFilter(filter=[string], useRegex=[boolean])
```

### Arguments


| Argument | Type | Required | Description | Default |
|----------|------|----------|-------------|---------|
| `filter` | `string` | `true` | The string pattern to match against. |  |
| `useRegex` | `boolean` | `false` | Use the regex filter instead of the wildcard filter. | `false` |

## Examples



## Related

  * [GetBoxCache](./GetBoxCache.md)
  * [GetBoxCacheNames](./GetBoxCacheNames.md)
  * [GetBoxCacheProviders](./GetBoxCacheProviders.md)
