= TYPED IDENTITY SYSTEM =

* COMPILE-TIME TYPE SAFETY FOR DISTRIBUTED SYSTEMS
* ELIMINATE STRINGLY-TYPED ID BUGS
* CROSS-LANGUAGE CONSISTENCY

== QUICK INSTALL ==

TypeScript:
  npm install @typedid/core

Rust:
  cargo add typedid

Go:
  go get github.com/typedid/go-core

== CORE CONCEPT ==

PROBLEM:
  User ID: "user_123"
  Post ID: "post_456" 
  But both are just strings - easy to mix up!

SOLUTION:
  User ID: UserID("user_123")  
  Post ID: PostID("post_456")
  Compiler prevents mixing them!

== LANGUAGE SUPPORT ==

TYPE-SCRIPT: PRODUCTION READY
  Features: Full type safety, serialization, validation

RUST: PRODUCTION READY  
  Features: Zero-copy, no_std support, serde

GO: BETA
  Features: Interface-based, JSON marshaling

== EXAMPLE USAGE ==

// TYPE-SCRIPT
const userId = UserID.create();
const postId = PostID.generate();
// userId == postId → COMPILE ERROR!

// RUST
let user_id = UserID::new();
let post_id = PostID::parse("post_abc")?;
// user_id == post_id → TYPE MISMATCH!

// GO
userId := typedid.NewUserID()
postId := typedid.NewPostID() 
// userId == postId → COMPILE TIME CHECK

== PROJECT INFO ==

Version: 1.2.0
License: Apache 2.0
Status: Active Development
Last Update: 2025-10-15

== LINKS ==

Documentation: https://typedid.dev/docs
API Reference: https://api.typedid.dev
Examples: https://github.com/typedid/examples

