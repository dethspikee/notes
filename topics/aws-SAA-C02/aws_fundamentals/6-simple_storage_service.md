<h1>S3</h1>

S3 is global storage platform - it's a public service, can be accessed from anywhere. S3 is regionally based, your data is stored in a specific AWS region. It never leaves that region unless you specifically configure it to. S3 is regionally resilient meaning data is replicated across AZs in that region. However S3 has an ability to replicate data across multiple regions.

S3 is perfect for hosting large amount of data such as movies, audio, photos etc.

S3 can be access via variety of methods such as UI, CLI, AWS APIs, HTTP.

S3 should be thought as a "default" aws storage service.

S3 delivers two main things:
- buckets
- objects

Objects are data that S3 stores and buckets are containers for objects.

An object in s3 is made up of two main components and some associated metadata:
- object key (similar to filename), key identifies the object in bucket.
- object value is data itself, sequence of binary data representing file

The value of an object in S3 can range from 0 bytes up to 5TB.

Objects also have:
- Version ID
- Metadata
- Access control
- Subresources

Buckets are created in a specific AWS regions. This means that data inside a bucket has primary home region and never leaves that region unless configured otherwise.

Bucket is identifed by its bucket name. The name has to be globally unique. No other user and no other aws account can use the same bucket name if it has been already taken by somebody else.

Buckets can hold unlimited amount of objects.

S3 has no complex strucute, it's flat, all objects stored in a bucket are stored at the same level.

Summary:
- Bucket names are globally unique
- Bucket names must be 3-63 characters, all lower case, no underscores
- Start with a lowercase letter or a number
- Can't be IP formatted like 1.1.1.1
- There is a soft limit of 100 buckets per aws account and hard limit (aws support requested) of 1000 buckets

Object's main components:
key = name, value = data

S3 patterns and anti-patterns:
- S3 is an object storage system, not file or block storate system.
- You can't mount an s3 bucket as (K:\ or /images)