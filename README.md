# Learning Amazon Kinesis Development

The master branch provides completed code for the [Process Real-Time Stock Data Using KPL and KCL Tutorial][learning-kinesis]  in the [Kinesis Developer Guide][kinesis-developer-guide].

The tutorial uses KCL 2.2.9 to demonstrate how to send a stream of records to Kinesis Data Streams and implement an application that consumes and processes the records in near-real time. 

[learning-kinesis]:  https://docs.aws.amazon.com/streams/latest/dev/tutorial-stock-data-kplkcl.html
[kinesis-developer-guide]: http://docs.aws.amazon.com/kinesis/latest/dev/introduction.html

## To run

**Producer:** Load into an IDE and run `StockTradesWriter` class, or:

```
export AWS_PROFILE=kinesis-demo

mvn exec:java -Dexec.mainClass="com.amazonaws.services.kinesis.samples.stocktrades.writer.StockTradesWriter" -Dexec.args="YourStreamName eu-west-1"
```

**Processor (Consumer):**

Arguments are: _<table-name> <stream-name> <region>_:

```
export AWS_PROFILE=kinesis-demo

mvn exec:java -Dexec.mainClass="com.amazonaws.services.kinesis.samples.stocktrades.writer.StockTradesProcessor" -Dexec.args="tradeytrades CillasTrades eu-west-1"
```

## License Summary

This sample code is made available under the MIT-0 license. See the LICENSE file.
