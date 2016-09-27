
## Check that the order we expect methods to be called is correct

```
var calledOrder = 0;

lineBuilder.Setup(x => x.BuildCallReferenceLine(It.IsAny<Call>()))
    .Returns(new List<Line>())
    .Callback(() => Assert.AreEqual(0, calledOrder++));

lineBuilder.Setup(x => x.BuildLabourLines(It.IsAny<Call>(), It.IsAny<List<InvoiceBreakdown>>()))
    .Returns(new List<Line>())
    .Callback(() => Assert.AreEqual(1, calledOrder++));
```
