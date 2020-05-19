## `AzureBlobStorageActions`

Implementation of the IBlobStorage interface
```csharp
public class ArJaiSolutions.AzureStorage.ExtensionLibrary.AzureBlobStorageActions
    : IBlobStorage, IDisposable

```

Properties

| Type | Name | Summary | 
| --- | --- | --- | 
| `CloudBlobClient` | BlobClient | Cloud Blob Client, from the Storage Account set [ArJaiSolutions.AzureStorage.ExtensionLibrary.AzureBlobStorageActions.StorageAccount](ArJaiSolutions.AzureStorage.ExtensionLibrary.AzureBlobStorageActions#storageaccount)  This can be only set from the constructor of the Implementation of this Inteface | 
| `CloudStorageAccount` | StorageAccount | Cloud Storage account  THis can be only set from the constructor of the Implementation of this Inteface | 


Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `Task<Boolean>` | BlobExistsOnCloud(`String` blobObjectName) | Check if the blobObject/file exists on the Blob | 
| `Task<Boolean>` | BlobExistsOnCloud(`String` blobObjectName, `CancellationToken` ct) | Check if the blobObject/file exists on the Blob | 
| `Task<Boolean>` | ContainsValidBlob(`Uri` uri) | Checks if there is a valid Blob in the Given URI | 
| `Task` | CopyAsync(`String` oldBlobNameWithPath, `String` newBlobNameWithPath, `CancellationToken` ct) | Copy the blob file from old file location into the new location. | 
| `void` | Dispose() | Dispose the AzureBlobStorageAction | 
| `void` | Finalize() | Destructor | 
| `Task<ICloudBlob>` | GetBlobAsync(`String` blobName) | Get the blob with the given Name | 
| `Task<ICloudBlob>` | GetBlobAsync(`String` blobName, `CancellationToken` ct) | Get the blob with the given Name | 
| `Task<ICloudBlob>` | GetBlobByUriAsync(`Uri` uri) | Get the Blob for the Given URI | 
| `Task<String>` | GetBlobSASTokenAsync(`String` blobNameWithPath, `SharedAccessBlobPermissions` sharedAccessBlobPermissions = Read, `Nullable<DateTimeOffset>` sharedAccessStartTime = null, `Nullable<DateTimeOffset>` sharedAccessExpiryTime = null) | Get the SAS Token for the given blobName with path(if Any) | 
| `Task<String>` | GetContainerSASTokenAsync(`String` blobNameWithPath, `SharedAccessBlobPermissions` sharedAccessBlobPermissions = Read, `Nullable<DateTimeOffset>` sharedAccessStartTime = null, `Nullable<DateTimeOffset>` sharedAccessExpiryTime = null) | Get the SAS Token for the given Container | 
| `Task<IEnumerable<Uri>>` | GetFileURIs(`String` prefix) | asynchronous operation that returns a collection of URI of blob items in the container  that starts with the given <i>prefix</i> | 
| `Task<IEnumerable<Uri>>` | GetFileURIs(`String` prefix, `CancellationToken` ct) | asynchronous operation that returns a collection of URI of blob items in the container  that starts with the given <i>prefix</i> | 
| `Task<String>` | GetUriAsync(`String` blobNameWithPath, `Boolean` withSASToken = False, `SharedAccessBlobPermissions` sharedAccessBlobPermissions = Read, `Nullable<DateTimeOffset>` sharedAccessStartTime = null, `Nullable<DateTimeOffset>` sharedAccessExpiryTime = null) | Get the URI for the blobName with path(if Any)  Optional  - with SAS Token | 
| `Task` | MoveAsync(`String` oldBlobNameWithPath, `String` newBlobNameWithPath, `CancellationToken` ct) | Copy the blob file from old file location into the new location.  and delete the old file blob location. | 
| `Task<Stream>` | ReadAsync(`Uri` uri) | Read the blob object as stream for the given URI | 
| `Task<Stream>` | ReadAsync(`Uri` uri, `CancellationToken` ct) | Read the blob object as stream for the given URI | 
| `Task` | WriteAsync(`String` blobNameWithPath, `Stream` data) | Write the Stream data to the blob with the name with path | 
| `Task` | WriteAsync(`String` blobNameWithPath, `Stream` data, `CancellationToken` ct) | Write the Stream data to the blob with the name with path | 


## `IBlobStorage`

Blob Interface Extensions
```csharp
public interface ArJaiSolutions.AzureStorage.ExtensionLibrary.IBlobStorage
    : IDisposable

```

Properties

| Type | Name | Summary | 
| --- | --- | --- | 
| `CloudBlobClient` | BlobClient | Cloud Blob Client, from the Storage Account set [ArJaiSolutions.AzureStorage.ExtensionLibrary.IBlobStorage.StorageAccount](ArJaiSolutions.AzureStorage.ExtensionLibrary.IBlobStorage#storageaccount)  This can be only set from the constructor of the Implementation of this Inteface | 
| `CloudStorageAccount` | StorageAccount | Cloud Storage account  THis can be only set from the constructor of the Implementation of this Inteface | 


Methods

| Type | Name | Summary | 
| --- | --- | --- | 
| `Task<Boolean>` | BlobExistsOnCloud(`String` blobObjectName) | Check if the blobObject/file exists on the Blob | 
| `Task<Boolean>` | BlobExistsOnCloud(`String` blobObjectName, `CancellationToken` ct) | Check if the blobObject/file exists on the Blob | 
| `Task<Boolean>` | ContainsValidBlob(`Uri` uri) | Checks if there is a valid Blob in the Given URI | 
| `Task` | CopyAsync(`String` oldBlobNameWithPath, `String` newBlobNameWithPath, `CancellationToken` ct) | Copy the blob file from old file location into the new location. | 
| `Task<ICloudBlob>` | GetBlobAsync(`String` blobName) | Get the blob with the given blob name | 
| `Task<ICloudBlob>` | GetBlobAsync(`String` blobName, `CancellationToken` ct) | Get the blob with the given blob name | 
| `Task<ICloudBlob>` | GetBlobByUriAsync(`Uri` uri) | Get the Blob for the Given URI | 
| `Task<String>` | GetBlobSASTokenAsync(`String` blobNameWithPath, `SharedAccessBlobPermissions` sharedAccessBlobPermissions = Read, `Nullable<DateTimeOffset>` sharedAccessStartTime = null, `Nullable<DateTimeOffset>` sharedAccessExpiryTime = null) | Get the SAS Token for the given blobName with path(if Any) | 
| `Task<String>` | GetContainerSASTokenAsync(`String` blobNameWithPath, `SharedAccessBlobPermissions` sharedAccessBlobPermissions = Read, `Nullable<DateTimeOffset>` sharedAccessStartTime = null, `Nullable<DateTimeOffset>` sharedAccessExpiryTime = null) | Get the SAS Token for the given Container | 
| `Task<IEnumerable<Uri>>` | GetFileURIs(`String` prefix) | asynchronous operation that returns a collection of URI of blob items in the container  that starts with the given <i>prefix</i> | 
| `Task<IEnumerable<Uri>>` | GetFileURIs(`String` prefix, `CancellationToken` ct) | asynchronous operation that returns a collection of URI of blob items in the container  that starts with the given <i>prefix</i> | 
| `Task<String>` | GetUriAsync(`String` blobNameWithPath, `Boolean` withSASToken = False, `SharedAccessBlobPermissions` sharedAccessBlobPermissions = Read, `Nullable<DateTimeOffset>` sharedAccessStartTime = null, `Nullable<DateTimeOffset>` sharedAccessExpiryTime = null) | Get the URI for the blobName with path(if Any)  Optional  - with SAS Token | 
| `Task` | MoveAsync(`String` oldBlobNameWithPath, `String` newBlobNameWithPath, `CancellationToken` ct) | Copy the blob file from old file location into the new location.  and delete the old file blob location. | 
| `Task<Stream>` | ReadAsync(`Uri` uri) | Read the blob object as stream for the given URI | 
| `Task<Stream>` | ReadAsync(`Uri` uri, `CancellationToken` ct) | Read the blob object as stream for the given URI | 
| `Task` | WriteAsync(`String` blobNameWithPath, `Stream` data) | Write the Stream data to the blob with the name with path | 
| `Task` | WriteAsync(`String` blobNameWithPath, `Stream` data, `CancellationToken` ct) | Write the Stream data to the blob with the name with path | 


