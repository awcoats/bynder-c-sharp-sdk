# Bynder C# SDK

[![Build Status](https://travis-ci.org/Bynder/bynder-c-sharp-sdk.svg?branch=master)](https://travis-ci.org/Bynder/bynder-c-sharp-sdk)

The main goal of this SDK is to speed up the integration of Bynder customers who use C# making it easier to connect to the Bynder API (http://docs.bynder.apiary.io) and executing requests on it.

## Nuget Package

You can download and use Bynder SDK from Nuget. https://www.nuget.org/packages/Bynder.Sdk/

## Current status

At the moment this SDK provides a library with the following methods:

### OAuth operations

```c#
string GetAuthorisationUrl(string state, string scopes);
Task GetAccessTokenAsync(string code, string scopes);
```

### Asset management operations

```c#
Task<IList<Brand>> GetBrandsAsync();
Task<Uri> GetDownloadFileUrlAsync(DownloadMediaQuery query);
Task<IDictionary<string, Metaproperty>> GetMetapropertiesAsync();
Task<Media> GetMediaInfoAsync(MediaInformationQuery query);
Task<IList<Media>> GetMediaListAsync(MediaQuery query);
Task UploadFileAsync(UploadQuery query);
Task ModifyMediaAsync(ModifyMediaQuery query);
```

### Collection management operations

```c#
Task<IList<Collection>> GetCollectionsAsync(GetCollectionsQuery query);
Task<Collection> GetCollectionAsync(string id);
Task CreateCollectionAsync(CreateCollectionQuery query);
Task DeleteCollectionAsync(string id);
Task<IList<string>> GetMediaAsync(GetMediaQuery query);
Task AddMediaAsync(AddMediaQuery query);
Task RemoveMediaAsync(RemoveMediaQuery query);
Task ShareCollectionAsync(ShareQuery query);
```

## Sample

To see how to use the SDK, please check [ApiSample.cs](Bynder/Sample/ApiSample.cs)
