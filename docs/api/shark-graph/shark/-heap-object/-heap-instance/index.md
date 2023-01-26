//[shark-graph](../../../../index.md)/[shark](../../index.md)/[HeapObject](../index.md)/[HeapInstance](index.md)

# HeapInstance

[jvm]\
class [HeapInstance](index.md) : [HeapObject](../index.md)

An instance in the heap dump.

## Functions

| Name | Summary |
|---|---|
| [get](get.md) | [jvm]<br>operator fun [get](get.md)(declaringClassName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), fieldName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [HeapField](../../-heap-field/index.md)?<br>operator fun [get](get.md)(declaringClass: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)&lt;out [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt;, fieldName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [HeapField](../../-heap-field/index.md)? |
| [instanceOf](instance-of.md) | [jvm]<br>infix fun [instanceOf](instance-of.md)(className: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns true if this is an instance of the class named [className](instance-of.md) or an instance of a subclass of that class.<br>[jvm]<br>infix fun [instanceOf](instance-of.md)(expectedClass: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)&lt;*&gt;): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>infix fun [instanceOf](instance-of.md)(expectedClass: [HeapObject.HeapClass](../-heap-class/index.md)): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns true if this is an instance of [expectedClass](instance-of.md) or an instance of a subclass of that class. |
| [readAsJavaString](read-as-java-string.md) | [jvm]<br>fun [readAsJavaString](read-as-java-string.md)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?<br>If this [HeapInstance](index.md) is an instance of the [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) class, returns a [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) instance with content that matches the string in the heap dump. Otherwise returns null. |
| [readField](read-field.md) | [jvm]<br>fun [readField](read-field.md)(declaringClassName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), fieldName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [HeapField](../../-heap-field/index.md)?<br>Returns a [HeapField](../../-heap-field/index.md) object that reflects the specified declared field of the instance represented by this [HeapInstance](index.md) object, or null if this field does not exist. The [declaringClassName](read-field.md) specifies the class in which the desired field is declared, and the [fieldName](read-field.md) parameter specifies the simple name of the desired field.<br>[jvm]<br>fun [readField](read-field.md)(declaringClass: [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)&lt;out [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)&gt;, fieldName: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)): [HeapField](../../-heap-field/index.md)? |
| [readFields](read-fields.md) | [jvm]<br>fun [readFields](read-fields.md)(): [Sequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/-sequence/index.html)&lt;[HeapField](../../-heap-field/index.md)&gt;<br>The fields of this instance, as a sequence of [HeapField](../../-heap-field/index.md). |
| [readRecord](read-record.md) | [jvm]<br>open override fun [readRecord](read-record.md)(): HprofRecord.HeapDumpRecord.ObjectRecord.InstanceDumpRecord<br>Reads and returns the underlying InstanceDumpRecord. |
| [toString](to-string.md) | [jvm]<br>open override fun [toString](to-string.md)(): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

## Properties

| Name | Summary |
|---|---|
| [asClass](../as-class.md) | [jvm]<br>val [asClass](../as-class.md): [HeapObject.HeapClass](../-heap-class/index.md)?<br>This [HeapObject](../index.md) as a [HeapClass](../-heap-class/index.md) if it is one, or null otherwise |
| [asInstance](../as-instance.md) | [jvm]<br>val [asInstance](../as-instance.md): [HeapObject.HeapInstance](index.md)?<br>This [HeapObject](../index.md) as a [HeapInstance](index.md) if it is one, or null otherwise |
| [asObjectArray](../as-object-array.md) | [jvm]<br>val [asObjectArray](../as-object-array.md): [HeapObject.HeapObjectArray](../-heap-object-array/index.md)?<br>This [HeapObject](../index.md) as a [HeapObjectArray](../-heap-object-array/index.md) if it is one, or null otherwise |
| [asPrimitiveArray](../as-primitive-array.md) | [jvm]<br>val [asPrimitiveArray](../as-primitive-array.md): [HeapObject.HeapPrimitiveArray](../-heap-primitive-array/index.md)?<br>This [HeapObject](../index.md) as a [HeapPrimitiveArray](../-heap-primitive-array/index.md) if it is one, or null otherwise |
| [byteSize](byte-size.md) | [jvm]<br>val [byteSize](byte-size.md): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) |
| [graph](graph.md) | [jvm]<br>open override val [graph](graph.md): [HeapGraph](../../-heap-graph/index.md)<br>The graph of objects in the heap, which you can use to navigate the heap. |
| [instanceClass](instance-class.md) | [jvm]<br>val [instanceClass](instance-class.md): [HeapObject.HeapClass](../-heap-class/index.md)<br>The class of this instance. |
| [instanceClassId](instance-class-id.md) | [jvm]<br>val [instanceClassId](instance-class-id.md): [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)<br>The heap identifier of the class of this instance. |
| [instanceClassName](instance-class-name.md) | [jvm]<br>val [instanceClassName](instance-class-name.md): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>The name of the class of this instance, identical to [Class.getName](https://docs.oracle.com/javase/8/docs/api/java/lang/Class.html#getName--). |
| [instanceClassSimpleName](instance-class-simple-name.md) | [jvm]<br>val [instanceClassSimpleName](instance-class-simple-name.md): [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)<br>Returns [instanceClassName](instance-class-name.md) stripped of any string content before the last period (included). |
| [isPrimitiveWrapper](is-primitive-wrapper.md) | [jvm]<br>val [isPrimitiveWrapper](is-primitive-wrapper.md): [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Whether this is an instance of a primitive wrapper type. |
| [objectId](object-id.md) | [jvm]<br>open override val [objectId](object-id.md): [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)<br>The heap identifier of this object. |
| [objectIndex](object-index.md) | [jvm]<br>open override val [objectIndex](object-index.md): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>An positive object index that's specific to how Shark stores objects in memory. The index starts at 0 and ends at [HeapGraph.objectCount](../../-heap-graph/object-count.md) - 1. There are no gaps, every index value corresponds to an object. Classes are first, then instances, then object arrays then primitive arrays. |
| [recordSize](record-size.md) | [jvm]<br>open override val [recordSize](record-size.md): [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)<br>The total byte size for the record of this object in the heap dump. |