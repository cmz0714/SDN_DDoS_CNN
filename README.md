# Experiment

## File Structure
- cnn/
    - training.py (deprecated)
        - CNN InceptionV3 training script with Keras (use [model/InceptionV3](https://github.com/tensorflow/models/tree/master/research/inception) with Tensorflow instead)
- darpa/
    - attack_analysis.py
        - Script that parses the TCPDUMP files extracted from DARPA1998.
    - attack_analysis.sh
        - `attack_analysis.py` running script.
    - sample_data01.tcpdump
        - Sample TCPDUMP file
        - The full list of DARPA1998 TCPDUMP files can be found in [DARPA1998](https://www.ll.mit.edu/r-d/datasets/1998-darpa-intrusion-detection-evaluation-data-set).
- image/
    - draw.py
        - Script that uses to generate images for CNN training.
- mininet/
    - easy_run.py
        - Experiment scene as paper described. 
    - run.sh
        - `easy_run.py` running script.
    - topo.jpg (deprecated)
    - topo.py (deprecated)
- raw_data/ 
    - tcpdump_regenerator.py 
        - Regenerating the traffic in DARPA1998 in the way of importing the TCPDUMP files into a Openvswitch (as paper described).
    - tcpdump_regenerator_print.py (deprecated)
    - tcpdumo_separator.sh
        - Separating TCPDUMP files into smaller one for further processing.
    - run.sh
        - `tcpdumo_separator.sh` running script.
- ryu/
    - app_realtime.py (deprecated)
    - app.py
        - Experimental controller.
    - monitor.py
        - Capturing the network state and stats in intervals.
- scapy/
    - attack_tools/
        - icmpflood.py
        - synflood.py
        - udpflood.py
    - realtime_tcpdump_regenerator.py (deprecated)
    - realtime_tcpdumplist_regenerator.py (deprecated)
- stat/
    - figure/
        - The result of experiment that test the performance of 31 network features.
            - Red dots represent abnormal situation (being attack).
                - The attack traffic is generated by the scripts in `attack_tools`.
                - DARPA1998 week3 data traffic + generated traffic
            - Blue dots represent normal situation.
                - DARPA1998 week3 data traffic only
            - 10 secs/sample.
    - image_analysis.m
        - Script thats plot the result of experiment with Matlab.
    - scatter_script.m (deprecated)
    - treshold_script.m (deprecated)