all: pupil_tracking_main.o recording_tracking_main.o camera_tracking_main.o findEyeCenter.o helpers.o GazeTracker.o
	g++ pupil_tracking_main.o recording_tracking_main.o camera_tracking_main.o findEyeCenter.o helpers.o GazeTracker.o `pkg-config --cflags --libs opencv` -o pupil_tracker 

GazeTracker.o: GazeTracker.cpp GazeTracker.h
	g++ GazeTracker.cpp -c

recording_tracking_main.o: tracking/recording_tracking_main.cpp tracking/recording_tracking_main.h
	g++ tracking/recording_tracking_main.cpp -c

camera_tracking_main.o: tracking/camera_tracking_main.cpp tracking/camera_tracking_main.h
	g++ tracking/camera_tracking_main.cpp -c

pupil_tracking_main.o: pupil_tracking_main.cpp pupil_tracking_main.h
	g++ pupil_tracking_main.cpp -c

findEyeCenter.o: tracking/findEyeCenter.cpp tracking/findEyeCenter.h tracking/constants.h
	g++ tracking/findEyeCenter.cpp -c

helpers.o: tracking/helpers.cpp tracking/helpers.h
	g++ tracking/helpers.cpp -c

clean:
	rm *.o pupil_tracker

