# howto-deepfakes
Custom deepfakes, ordered deepfakes

Extract the training set from the targeting file After you clear your targeting file, you might want to drag some of these people to use for the training set. This is an easy task - as explained in https://deepfake-porn.com/howto-custom-deepfake/.

Go to the Tools tab and then the Align tab.

Jobs - This is a list of all the targeting jobs available in the tool.
Select "Extract".
Data - the location of the resource that we want to process.

Alignment file: Select the alignment file that was produced during cleaning in the last step. It's in the same folder as the video where you extracted it, or in the image folder where you extracted it.

Face folder: Select an empty folder where faces should be moved.
Frame folder: Select the video or frame folder that you use as input for the extraction process.
Leave all the other options in this section blank because there is no need for this step.

Extras - This is an option to extract faces from alignment files.
Extract every N: That depends on the number of frames per second. For videos with 25 frames per second, the normal value is between 12 and 25 (i.e. every half to second). Anything besides that and you might have too many similar faces. It's a good idea to consider how many sources you want to extract for your training kit, how many faces you want in your final training kit, and how long is your source. They all differ from case to case.

Size: This is the size of the image that the extracted person has. This time
Models over 256px are not supported. Leave this as the default.
Straighten your eyes: I find this option completely useless. Straightener has aligned the surface. No further alignment is needed.

Run - leave all other default options. We are now ready to review our features and extract our training kit from our clean alignment file in the folder we chose.
You should get a screen similar to the one below.
Press the Align button to extract the face.

If you practice with a mask or want to use Warp to Landmark, copy the alignment file from the location of your output frame to the newly created face folder.

Combine aspects of training So that some people are ready for training and many files are available to align the frame from where these people come from. Can they be combined into one training source? You might be able to!


Preparation - We need to prepare before we merge the targeting file.
First, copy everyone you want to train from each folder to the folder (we'll call it "Training" for reference).
Copy all the targeting files that apply to the person currently selected from their source frame location to the new training folder.

Now switch to the Tools tab in the GUI and then to the Align tab.

Jo - This is a list of all the targeting jobs available in the tool.
Select "Join".

Data - the location of the resource that we want to process.
Alignment files: Open your training folder, prepare a backup, and highlight all the alignment files that you just copied to select them.
Face folder: Select the training folder where you can enter all faces.
Leave all the other options in this section blank because there is no need for this step.

Run - leave all other default options. We are now ready to review our features and merge our alignment files.
You should get a screen similar to the one below.
Click the Align button to merge files.

Completion - When the process is complete:
Delete all the alignment files that you previously copied to the training folder from the training folder.
Change the name of the synchronization file generated in the training folder to "align.fsa".
Your training kit is ready.

To train the model, you need to extract both pairs of faces from the video to create a set of faces. For example, to replace Keanu Reeves and Nick Cage, you will pull Keanu and Nick's faces from various sources to make training kits for everyone. If the video also contains an unwanted face, just delete the unwanted face.

I mean, you can "save" several masks per person, not that you can use them. You can use the same mask (at this time) only for exercises A and B.

I haven't had the chance to appreciate a newer mask yet.
I do not recommend it. The order in which the detectors find faces is completely arbitrary. Suppose he finds two faces in a frame, one of which is a false positive. The right face can be in positions 0 and 1. If you delete all faces in position 1, you have a 50/50 chance of removing faces or false positives.

