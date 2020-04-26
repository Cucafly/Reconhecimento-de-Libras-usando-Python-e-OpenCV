# Libras-Recognition-using-Python-and-OpenCV

# Instructions
# The lines of code below must be executed in Google Colab. First save the files to your Google Drive. Then, create a directory. Obs .: the paths must be the same ones created and not the ones indicated in the lines of code below.

Hand - Translating Libras into images

For the more dynamic identification of various positions, 4 modules were developed to extract some characteristics and compare the displacement of the joints (key points)

We extract HEIGHT, POSITION and PROXIMITY between the detected key points

Module extrator_ALTURA: checks if a point is 'above' or 'below' another specific point. For example, if the fingertip is 'above' the wrist

Extrator_POSICAO module: functions to check if the fingers are 'bent' or 'stretched', horizontally or vertically. It also receives the result of the extractor_ALTURA module to know what position the hand is in (turned 'up' or 'down')

Extractor_PROXIMITY module: functions that compare the proximity between the detected key points. For example, if the result of the extractor_POSICAO module is equal to 'folded' for the index and middle fingers and both are at the same height, then it means that the fingers are close

Alphabet module: after extracting all these characteristics, the characteristics alphabet was created, where a VECTOR OF VECTORS receives the result of all the extractor modules. So we use this module to compare with a new analysis (new image) of input

The letters: H, J, K, X,, Y, Z were not used due to the additional movement for the correct execution of the letters.

These letters can be analyzed in a different function, similar to the body position analysis function, where we compare the transition between points

Letter T: for the thumb, due to being overlapped by the index finger, the algorithm does not recognize the points on the fingertip. Letter N and U are confused

Note: the algorithm is still being improved.
