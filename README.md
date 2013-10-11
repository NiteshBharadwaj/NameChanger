NameChanger
===========

Use jarjar to rename bouncycastle to spongycastle

This is a widely used method to rename classes inside a jar file. 
This is a very simple code which does nothing other than renaming.
For example, you can use the the original KeyFactory.getInstance("EC","BC") unlike some online versions which force branding with KeyFactory.getInstance("EC","SC").
The only change required in the java code is with the imports, where we import org.spongycastle.* instead of org.bouncycastle.*

You can ask "Why to rename?"

Good question, but with the android supporting only *some* part of bouncy castle and changing support on different versions. (of android), it produces the killer classname conflicts
Answer: To provide uniform standards on all versions of android and to avoid class name conflicts.

Pre-Requisite: Ant

How to use:

Put the bouncy castle jar file in 'build' folder.
Edit the build.xml file to put the correct file names.
Run using the command 'ant'.
Output jar file will be in 'dist' folder.
