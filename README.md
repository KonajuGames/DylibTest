# DylibTest
Repro project for Xamarin Mac dylib Native Reference in library project

1. Clone the repo.
2. Build the project.
3. Open the output app bundle and look for `libopenal.1.dylib`.  It should be in `DylibTest/bin/Debug/DylibTest.app/Contents/MonoBundle`, but you won't find it.
4. Remove the libopenal.1.dylib file from Native References in the DylibLibrary project.
5. Add DylibLibrary/libopenal.1.dylib as a Native Reference in the DylibTest project.
6. Build the project.
7. Open the output app bundle again and look for `libopenal.1.dylib`.  It should be in `DylibTest/bin/Debug/DylibTest.app/Contents/MonoBundle`, and it will now be there.
