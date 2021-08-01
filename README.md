# IBM-watson-speech-to-text-and-vice-versa

On the 4th task of the summer traing at smart company Int.

We followed the following instruction on this video.

https://www.youtube.com/watch?v=YCyuZM454_I



Requries:


Python
IBM watson account 
CMD
Coding Env (VSC e.g)
Git

we followed this documnation to connect the serverr to the python code:

https://cloud.ibm.com/apidocs/text-to-speech?code=python

we wrote the following code to create text and mp4 output files:


    with open('output.txt', 'r') as f:
            text = f.readlines()
    text = [line.replace('\n','') for line in text]
    text = ''.join(str(line) for line in text)
    with open('./output.mp3', 'wb') as audio_file:
        res = tts.synthesize(text, accept='audio/mp3', voice='en-GB_JamesV3Voice').get_result()
        audio_file.write(res.content) 


