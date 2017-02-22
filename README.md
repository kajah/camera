# camera

# build instructions
Uses the Camera2 API, so must have Android SDK 21+
Download and run in Android Studio

# further considerations
I began by exploring different ideas for how to store files locally. The first thing that came to mind was Android's internal storage, which is inherently secure - files will be saved to the app itself and will be deleted if the app is deleted. Internal storage is definitely more secure than external storage. Another thought was to use a viewfinder and just get an array of the bytes of the images when they are captured, but I would still have to store them somewhere. I also thought of using private keys (Keystore) to make the entire app more secure, so the pictures saved internally in the app will have another layer of security. Due to time constraints, I stuck with just saving the pictures to the app's internal storage.

Unfortunately, I have didn't have any experience with Android's camera APIs before this challenge. Therefore I spend a significant amount of time implementing the Camera using the Camera2 API. I have a good idea about how to implement take 10 pictures in 5 seconds, using the CameraCaptureSession, however, I did not have time to implement it.

Another issue is that creating the capture session fails, therefore the picture taken cannot be saved. However, I did implement saving the picture to internal storage, if you refer to the takePicture() function.

I added another button to the app so that users would have time to get in a desired position before hitting "Take Picture". For making this app better, I would maybe encrypt the pictures taken when saving them. I would also maybe add preferences so users can choose how many pictures the app takes in a burst.
