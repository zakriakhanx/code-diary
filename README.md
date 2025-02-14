

## 2025-02-14 23:51:57 - Backend

fix(auth): Correct typo in signin route console log

```diff
diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
-    console.log('this is test 2 from route signi')
+    console.log('this is test 2 from route signin')

```

## 2025-02-15 00:09:17 - Backend

chore(auth): Update console log message in signin route

```diff
diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
-    console.log('this is test message from route sign ')
+    console.log('this is test message from route signin ')

```

## 2025-02-15 00:10:45 - Backend

fix(auth): Correct console log message in signout function

```diff
diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
-    console.log('this is test 2 from signo')
+    console.log('this is test 2 from signout')

```

## 2025-02-15 00:18:38 - Backend

chore(auth): Add console log placeholder in signOut function

```diff
diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    
+    co
 }

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    co
+    com
 }

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    com
+    co
 }

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    co
+    con
 }

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    con
+    conso
 }

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    conso
+    consol
-}
+

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    consol
+    console
-
+}

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    console
+    console.
 }

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    console.
+    console.l
 }

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    console.l
+    console.log
 }

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    console.log
+    console.log()
 }

diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,59 +1,59 @@
 }
 
 export const signOut = async (req, res, next) => {
-    console.log()
+    console.log('')
 }

```

## 2025-02-15 00:39:44 - Backend

chore(auth): Add test message to signOut controller

```diff
diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,${oldLines.length} +1,${newLines.length} @@
 }
 
 export const signOut = async (req, res, next) => {
-    
+    console.log('this is test message from signout')
 }

```

## 2025-02-15 00:43:00 - Backend

fix(auth): Update auth controller with proper error handling and response formatting

```diff
diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,${oldLines.length} +1,${newLines.length} @@

```

## 2025-02-15 00:44:06 - Backend

refactor(auth): Remove signUp functionality and clean up auth controller

```diff
diff --git a/controllers\auth.controller.js b/controllers\auth.controller.js
--- a/controllers\auth.controller.js
+++ b/controllers\auth.controller.js
@@ -1,${oldLines.length} +1,${newLines.length} @@
 import jwt from "jsonwebtoken";
 import { JWT_EXPIRES_IN, JWT_SECRET } from "../config/env.js";
 
-export const signUp = async (req, res, next) => {
+
-    //atomic operation
+
-    const session = await mongoose.startSession();
+export const signIn = async (req, res, next) => {
-    session.startTransaction();
+    console.log('this is test message from signIn')
-    
+}
-    try { //logic to create new user
+
-        
+export const signOut = async (req, res, next) => {
-        const { name, email, password } = req.body;
+    console.log('this is test message from signout')
-
+}
-        // Check if a user already exists
-        const existingUser = await User.findOne({email});
-
-        if(existingUser){
-            const error = new Error('User already exists');
-            error.statusCode = 409;
-            throw error;
-        }
-
-        // Hash password
-        const salt = await bcrypt.genSalt(10);
-        const hashedPassword = await bcrypt.hash(password, salt);
-
-        const newUsers = await User.create([{ name, email, password: hashedPassword }], { session });
-
-        const token = jwt.sign({ userId: newUsers[0]._id }, JWT_SECRET, { expiresIn: JWT_EXPIRES_IN });
-
-        await session.commitTransaction();
-        session.endSession();
-
-        res.status(201).json({
-            success: true,
-            message: 'User created successfully',
-            data: {
-                token,
-                user: newUsers[0]
-            }
-        })
-
-    } catch (error) {
-        await session.abortTransaction();
-        session.endSession();
-        next(error);
-
-    }
-}
-
-export const signIn = async (req, res, next) => {
-    console.log('this is test message from signIn')
-}
-
-export const signOut = async (req, res, next) => {
-    console.log('this is test message from signout')
-}

```
