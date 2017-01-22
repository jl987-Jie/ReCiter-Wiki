# Check Performance

In order to check the average precision and recall of ReCiter, you can execute the following MongoDB query.

```MongoDB
db.analysis.aggregate([
{
	$group: {
		_id:null, precision: {$avg:"$analysis.precision"}, recall: {$avg:"$analysis.recall"}
	}
}
]);
```



