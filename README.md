# BigAzureStorage
Utility functions for Azure Storage C# API
## BigAzureTable
Many of the common actions in the `Microsoft.WindowsAzure.Storage.Table` library are limited to some X amount of operations per request, like query will return 100 entities per request (or something like that) and then return a continuation token, or executing a batch operation is limited to 100 operations per batch.  The Microsoft library doesn't provide anything built in to break up those operations into a single call like `table.ExecuteMyBatch(bigBatch)`, instead you'd have to break it up and run it multiple times.
