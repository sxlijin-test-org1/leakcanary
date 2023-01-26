//[shark-hprof](../../index.md)/[shark](index.md)

# Package shark

## Types

| Name | Summary |
|---|---|
| [ByteArraySourceProvider](-byte-array-source-provider/index.md) | [jvm]<br>class [ByteArraySourceProvider](-byte-array-source-provider/index.md)(byteArray: [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)) : [DualSourceProvider](-dual-source-provider/index.md) |
| [ConstantMemoryMetricsDualSourceProvider](-constant-memory-metrics-dual-source-provider/index.md) | [jvm]<br>class [ConstantMemoryMetricsDualSourceProvider](-constant-memory-metrics-dual-source-provider/index.md)(realSourceProvider: [DualSourceProvider](-dual-source-provider/index.md)) : [DualSourceProvider](-dual-source-provider/index.md)<br>Captures IO read metrics without using much memory. |
| [DualSourceProvider](-dual-source-provider/index.md) | [jvm]<br>interface [DualSourceProvider](-dual-source-provider/index.md) : [StreamingSourceProvider](-streaming-source-provider/index.md), [RandomAccessSourceProvider](-random-access-source-provider/index.md)<br>Both a [StreamingSourceProvider](-streaming-source-provider/index.md) and a [RandomAccessSourceProvider](-random-access-source-provider/index.md) |
| [FileSourceProvider](-file-source-provider/index.md) | [jvm]<br>class [FileSourceProvider](-file-source-provider/index.md)(file: [File](https://docs.oracle.com/javase/8/docs/api/java/io/File.html)) : [DualSourceProvider](-dual-source-provider/index.md) |
| [GcRoot](-gc-root/index.md) | [jvm]<br>sealed class [GcRoot](-gc-root/index.md)<br>A GcRoot as identified by [HprofRecord.HeapDumpRecord.GcRootRecord](-hprof-record/-heap-dump-record/-gc-root-record/index.md) in the heap dump. |
| [HprofDeobfuscator](-hprof-deobfuscator/index.md) | [jvm]<br>class [HprofDeobfuscator](-hprof-deobfuscator/index.md)<br>Converts a Hprof file to another file with deobfuscated class and field names. |
| [HprofHeader](-hprof-header/index.md) | [jvm]<br>data class [HprofHeader](-hprof-header/index.md)(heapDumpTimestamp: [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html), version: [HprofVersion](-hprof-version/index.md), identifierByteSize: [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html))<br>Represents the header metadata of a Hprof file. |
| [HprofPrimitiveArrayStripper](-hprof-primitive-array-stripper/index.md) | [jvm]<br>class [HprofPrimitiveArrayStripper](-hprof-primitive-array-stripper/index.md)<br>Converts a Hprof file to another file with all primitive arrays replaced with arrays of zeroes, which can be useful to remove PII. Char arrays are handled slightly differently because 0 would be the null character so instead these become arrays of '?'. |
| [HprofRecord](-hprof-record/index.md) | [jvm]<br>sealed class [HprofRecord](-hprof-record/index.md)<br>A Hprof record. These data structure map 1:1 with how records are written in hprof files. |
| [HprofRecordReader](-hprof-record-reader/index.md) | [jvm]<br>class [HprofRecordReader](-hprof-record-reader/index.md)<br>Reads hprof content from an Okio [BufferedSource](https://square.github.io/okio/2.x/okio/okio/-buffered-source/index.html). |
| [HprofRecordTag](-hprof-record-tag/index.md) | [jvm]<br>enum [HprofRecordTag](-hprof-record-tag/index.md) : [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)&lt;[HprofRecordTag](-hprof-record-tag/index.md)&gt; |
| [HprofVersion](-hprof-version/index.md) | [jvm]<br>enum [HprofVersion](-hprof-version/index.md) : [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)&lt;[HprofVersion](-hprof-version/index.md)&gt; <br>Supported hprof versions |
| [HprofWriter](-hprof-writer/index.md) | [jvm]<br>class [HprofWriter](-hprof-writer/index.md) : [Closeable](https://docs.oracle.com/javase/8/docs/api/java/io/Closeable.html)<br>Generates Hprof files. |
| [OnHprofRecordListener](-on-hprof-record-listener/index.md) | [jvm]<br>fun interface [OnHprofRecordListener](-on-hprof-record-listener/index.md)<br>Listener passed in to [StreamingHprofReader.readRecords](-streaming-hprof-reader/read-records.md), gets notified for each [HprofRecord](-hprof-record/index.md) found in the heap dump which types is in the set of the recordTypes parameter passed to [StreamingHprofReader.readRecords](-streaming-hprof-reader/read-records.md). |
| [OnHprofRecordTagListener](-on-hprof-record-tag-listener/index.md) | [jvm]<br>fun interface [OnHprofRecordTagListener](-on-hprof-record-tag-listener/index.md)<br>Listener passed in to [StreamingHprofReader.readRecords](-streaming-hprof-reader/read-records.md), gets notified for each [HprofRecordTag](-hprof-record-tag/index.md) found in the heap dump. |
| [PrimitiveType](-primitive-type/index.md) | [jvm]<br>enum [PrimitiveType](-primitive-type/index.md) : [Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)&lt;[PrimitiveType](-primitive-type/index.md)&gt; <br>A primitive type in the prof. |
| [ProguardMapping](-proguard-mapping/index.md) | [jvm]<br>class [ProguardMapping](-proguard-mapping/index.md) |
| [ProguardMappingReader](-proguard-mapping-reader/index.md) | [jvm]<br>class [ProguardMappingReader](-proguard-mapping-reader/index.md)(proguardMappingInputStream: [InputStream](https://docs.oracle.com/javase/8/docs/api/java/io/InputStream.html)) |
| [RandomAccessHprofReader](-random-access-hprof-reader/index.md) | [jvm]<br>class [RandomAccessHprofReader](-random-access-hprof-reader/index.md) : [Closeable](https://docs.oracle.com/javase/8/docs/api/java/io/Closeable.html)<br>Reads records in a Hprof source, one at a time with a specific position and size. Call [openReaderFor](-random-access-hprof-reader/-companion/open-reader-for.md) to obtain a new instance. |
| [RandomAccessSource](-random-access-source/index.md) | [jvm]<br>interface [RandomAccessSource](-random-access-source/index.md) : [Closeable](https://docs.oracle.com/javase/8/docs/api/java/io/Closeable.html) |
| [RandomAccessSourceProvider](-random-access-source-provider/index.md) | [jvm]<br>fun interface [RandomAccessSourceProvider](-random-access-source-provider/index.md)<br>Can open [RandomAccessSource](-random-access-source/index.md) instances. |
| [StreamingHprofReader](-streaming-hprof-reader/index.md) | [jvm]<br>class [StreamingHprofReader](-streaming-hprof-reader/index.md)<br>Reads the entire content of a Hprof source in one fell swoop. Call [readerFor](-streaming-hprof-reader/-companion/reader-for.md) to obtain a new instance. |
| [StreamingRecordReaderAdapter](-streaming-record-reader-adapter/index.md) | [jvm]<br>class [StreamingRecordReaderAdapter](-streaming-record-reader-adapter/index.md)(streamingHprofReader: [StreamingHprofReader](-streaming-hprof-reader/index.md))<br>Wraps a [StreamingHprofReader](-streaming-hprof-reader/index.md) to provide a higher level API that streams [HprofRecord](-hprof-record/index.md) instances. |
| [StreamingSourceProvider](-streaming-source-provider/index.md) | [jvm]<br>fun interface [StreamingSourceProvider](-streaming-source-provider/index.md)<br>Can open [Source](https://square.github.io/okio/2.x/okio/okio/-source/index.html) instances. |
| [ThrowingCancelableFileSourceProvider](-throwing-cancelable-file-source-provider/index.md) | [jvm]<br>class [ThrowingCancelableFileSourceProvider](-throwing-cancelable-file-source-provider/index.md)(file: [File](https://docs.oracle.com/javase/8/docs/api/java/io/File.html), throwIfCanceled: [Runnable](https://docs.oracle.com/javase/8/docs/api/java/lang/Runnable.html)) : [DualSourceProvider](-dual-source-provider/index.md)<br>A [DualSourceProvider](-dual-source-provider/index.md) that invokes throwIfCanceled before every read, allowing cancellation of IO based work built on top by throwing an exception. |
| [ValueHolder](-value-holder/index.md) | [jvm]<br>sealed class [ValueHolder](-value-holder/index.md)<br>A value in the heap dump, which can be a [ReferenceHolder](-value-holder/-reference-holder/index.md) or a primitive type. |