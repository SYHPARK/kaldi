Thank you, stupid student!
https://groups.google.com/g/zeroth-help/c/P3v1CSP1Qjo

CAUTION: Don't forget "conda activate zeroth"

0. Kaldi compile: http://kaldi-asr.org/doc/tutorial_setup.html

1. First, check dependencies
/home/yongbak/kaldi_stt/tools/extras/check_dependencies.sh

In my case, I should execute install_mkl.sh.

When you see check_dependencies.sh: all OK, it's done

2. Follow the instructions for Kaldi compilation
https://kaldi-asr.org/doc/tutorial_setup.html

3. It might ask us to run tools/extra/install_morfessor.sh

After this, you have to run the env.sh below:
source {$KALDI_ROOT}/tools/extra/env.sh

Not the env.sh in
source {$KALDI_ROOT}/tools/env.sh

PLEASE make sure this
And be careful about "sourcing on bash shell, not zsh"

+)Read this page
https://jybaek.tistory.com/772
https://hanseokhyeon.tistory.com/entry/Kaldi-%EC%98%88%EC%A0%9C-Voxforge-%EB%8D%B0%EC%9D%B4%ED%84%B0

4. If queue.ql error occurs, change "queue.pl" into "run.pl" of cmd.sh.

Read the link carefully below:
https://stackoverflow.com/questions/51126825/kaldi-output-of-qsub-was-qsub-illegal-c-value-when-trying-to-run-the-comm
http://kaldi-asr.org/doc/queue.html

5. If out of memory error occurs, scheme the website below:
https://groups.google.com/g/zeroth-help/c/KX10wh1NUyw

How to solve:
1. run "nvidia-smi --compute-mode=3" on terminal
2. "--use-gpu" at run.sh: "yes" -> "wait"

6. refer to "https://bourbonkk.tistory.com/28"


--------------------------------------------
1. kaldi compile: https://groups.google.com/g/zeroth-help/c/P3v1CSP1Qjo
2. download zeroth repo, and put it into "egs"
3. follow "https://bourbonkk.tistory.com/28"