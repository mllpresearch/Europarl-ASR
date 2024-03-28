<!-- Etiquetatge JSON-LD generat per l'Assistent per a l'etiquetatge de dades estructurades de Google. -->
<!--
<script type="application/ld+json">
{
  "@context": "http://schema.org",
  "@type": "Dataset",
  "name": "Europarl-ASR",
  "description": "A 1300-hour English-language speech and text corpus of parliamentary debates for (streaming) ASR training and benchmarking, speech data filtering and speech data verbatimization.",
  "temporalCoverage": "1996 to 2020",
  "spatialCoverage": "European Parliament",
  "version": "v1.0",
  "license": "CC BY 4.0",
  "distribution": {
    "@type": "DataDownload",
    "encodingFormat": ".tar.gz",
    "contentUrl": "https://www.mllp.upv.es/europarl-asr/Europarl-ASR_v1.0.tar.gz"
  },
  "sourceOrganization": "Universitat Politècnica de València",
  "datePublished": "2021-04-02"
}
</script>
-->

# Europarl-ASR
Europarl-ASR v1.0  
2 April 2021  
[www.mllp.upv.es/europarl-asr](https://www.mllp.upv.es/europarl-asr)

A 1300-hour English-language speech and text corpus of parliamentary debates for
(streaming) ASR training and benchmarking, speech data filtering and speech data verbatimization.

Keywords: automatic speech recognition; speech corpus; speech data filtering;
speech data verbatimization.

CONTACT:
Gonçal V. Garcés Díaz-Munío (gogardia@vrain.upv.es),
Joan Albert Silvestre-Cerdà (jsilvestre@vrain.upv.es).
Universitat Politècnica de València.


README CONTENTS
---------------

- [Overview](#overview)
- [Citation](#citation)
- [Get the data](#get-the-data)
- [Additional Europarl-ASR materials](#additional-europarl-asr-materials)
- [Corpus structure and contents](#corpus-structure-and-contents)
- [Extended description](#extended-description)
- [Acknowledgements](#acknowledgements)
- [Legal disclaimers](#legal-disclaimers)
- [Licence](#licence)


OVERVIEW
--------

Europarl-ASR (EN) includes:

#### Speech data

* 1300 hours of English-language annotated speech data.
* 3 full sets of timed transcriptions: official non-verbatim transcriptions,
  automatically noise-filtered transcriptions and automatically verbatimized
  transcriptions.
* 18 hours of speech data with both manually revised verbatim transcriptions
  and official non-verbatim transcriptions, split in 2 independent
  validation-evaluation partitions for 2 realistic ASR tasks (with vs. without previous
  knowledge of the speaker).


#### Text data

* 70 million tokens of English-language text data.

#### Pretrained language models

* The Europarl-ASR English-language n-gram language model and vocabulary.

This data comprises most of the European Parliament's English-language debate
recordings, transcriptions and translations available from the Parliament's
website from 1996 to 2020. Additionally, to increase text data up to 170M
tokens, Europarl-ASR also includes tools to add all English-language text from
the DCEP Digital Corpus of the European Parliament.

CITATION
--------
http://dx.doi.org/10.21437/Interspeech.2021-1905

Garcés Díaz-Munío, Gonçal V.; Silvestre-Cerdà, Joan Albert; Jorge, Javier; Giménez, Adrià; Iranzo-Sánchez, Javier; Baquero-Arnal, Pau; Roselló, Nahuel; Pérez-González-de-Martos, Alejandro; Civera, Jorge; Sanchis, Albert; Juan, Alfons. "Europarl-ASR: A Large Corpus of Parliamentary Debates for Streaming ASR Benchmarking and Speech Data Filtering/Verbatimization". In Proc. Interspeech 2021, pp. 3695–3699, Brno (Czech Republic), 2021.

```
@inproceedings{europarlasr2021,
title = {{Europarl-ASR: A Large Corpus of Parliamentary Debates for Streaming ASR Benchmarking and Speech Data Filtering/Verbatimization}},
author = {Garcés Díaz-Munío, Gonçal V. and Silvestre-Cerdà, Joan Albert and Javier Jorge and Adrià Giménez and Javier Iranzo-Sánchez and Pau Baquero-Arnal and Nahuel Roselló and Alejandro Pérez-González-de-Martos and Jorge Civera and Albert Sanchis and Alfons Juan},
booktitle = {Proc. Interspeech 2021},
pages={3695--3699},
address = {Brno (Czech Republic)},
year = 2021,
doi={10.21437/Interspeech.2021-1905}
}
```

GET THE DATA
------------

Download the full Europarl-ASR speech and text corpus from:

https://www.mllp.upv.es/europarl-asr/Europarl-ASR_v1.0.tar.gz  
Size: 18 GiB  
SHA-256 checksum: 4d360170ef8f1d1ece55566eda4211274b27328427a3443061f43d80d3346e74

ADDITIONAL Europarl-ASR MATERIALS
---------------------------------

In addition to the speech and text data included in the main release and
described in this document, we are making available for download the following
materials to facilitate the reproducibility of our experiments:

* The pretrained Europarl-ASR English-language n-gram language model, together
  with its vocabulary file:    
  https://www.mllp.upv.es/europarl-asr/Europarl-ASR_v1.0_ngram_lm_and_vocab.tar.gz  
  Size: 1,1 GiB  
  SHA-256 checksum: 2be8eb7918086a233545e6e5a0592b7ae83a09ffb5ce479b68e28329d710cd6a

* The Europarl-ASR English-language verbatim transcription guidelines, which
  were applied to produce the manually revised verbatim transcriptions for the
  dev and test sets:    
  https://www.mllp.upv.es/europarl-asr/Europarl-ASR_transcription_guidelines.pdf  
  Size: 309 KiB  
  SHA-256 checksum: 66dac867b76c984d9e583caab0a8fd7540a664017e88e9ec4190c90ab67ce8e6


CORPUS STRUCTURE AND CONTENTS
-----------------------------

Total size: 18 GiB

The data is organized in 3 main directories: "train" (training data), "dev"
(validation data) and "test" (evaluation data). Each directory contains the
subdirectories "original_audio" and "text", the first one containing speech
data with annotations (for acoustic modelling), the second one containing text
data (for language modelling).

Here we can see more completely the corpus structure, with additional
subdirectories:

```
  Europarl-ASR
  └── en
      ├── dev
      │   ├── original_audio
      │   │   ├── spk-dep
      │   │   │   ├── lists
      │   │   │   ├── metadata
      │   │   │   ├── refs
      │   │   │   └── speeches
      │   │   └── spk-indep
      │   │       ├── lists
      │   │       ├── metadata
      │   │       ├── refs
      │   │       └── speeches
      │   └── text
      │       ├── prepro
      │       └── raw
      ├── test
      │   ├── original_audio
      │   │   ├── spk-dep
      │   │   │   ├── lists
      │   │   │   ├── metadata
      │   │   │   ├── refs
      │   │   │   └── speeches
      │   │   └── spk-indep
      │   │       ├── lists
      │   │       ├── metadata
      │   │       ├── refs
      │   │       └── speeches
      │   └── text
      │       ├── prepro
      │       └── raw
      └── train
          ├── original_audio
          │   ├── lists
          │   ├── metadata
          │   └── speeches
          └── text
              ├── external
              │   ├── prepro
              │   └── scripts
              └── internal
                  ├── prepro
                  └── raw
```

#### Speech data ("original_audio" directories)

In the cases of "dev" and "test", they are subdivided in directories "spk-dep"
and "spk-indep". Thus, for speech data, we have 2 train-dev-test partitions
for 2 different ASR tasks, as follows:

1. ASR with known speakers (MEP):  
   train ; dev/original_audio/spk-dep ; test/original_audio/spk-dep
   
1. ASR with unknown speakers (Guest):  
   train ; dev/original_audio/spk-indep ; test/original_audio/spk-indep

Each of these partition directories contains 3 to 4 subdirectories (depending
on whether it is the train set or the dev/test sets): "lists", "metadata",
"refs" (only in "dev" and "test") and "speeches".

"lists" contains lists of all the speeches in "speeches", as well as lists of
speeches per speaker.

"metadata" contains metadata for each speech and for each speaker in the
corresponding set (as csv and json files). For each speech we will find these
metadata (as reflected in speeches.headers.csv):

&nbsp;&nbsp;&nbsp;&nbsp;term;session_date;speech_id;speaker_type;speaker_id;raw_dur;  
&nbsp;&nbsp;&nbsp;&nbsp;aligned-speech_dur;filtered-speech_dur;cer;ar;path;agenda_item_title

And for each speaker (as reflected in speakers.headers.csv):

&nbsp;&nbsp;&nbsp;&nbsp;type;id;name;gender;url

"speeches" contains a subdirectory for each speech in the corresponding set,
according to this subdirectory structure:

&nbsp;&nbsp;&nbsp;&nbsp;`speeches/<term>/<session_date>/<speech_id>/`

For each speech, we will find some of the following files (depending on
whether it is in the train set or in the dev/test sets):

&nbsp;&nbsp;&nbsp;&nbsp;`ep-asr.en.orig.<term>.<session_date>.<speech_id>.m4a`  
&nbsp;&nbsp;&nbsp;&nbsp;[In all sets] Audio of the speech.

&nbsp;&nbsp;&nbsp;&nbsp;`ep-asr.en.orig.<term>.<session_date>.<speech_id>.tr.orig.{dfxp,json,srt,txt}`  
&nbsp;&nbsp;&nbsp;&nbsp;[In all sets] Official non-verbatim transcription of the speech, as a txt
  raw transcription file, as dfxp or srt force-aligned timed subtitle files,
  and its json metadata.

&nbsp;&nbsp;&nbsp;&nbsp;`ep-asr.en.orig.<term>.<session_date>.<speech_id>.tr.filt.{dfxp,json,srt}`  
&nbsp;&nbsp;&nbsp;&nbsp;[In train set] Automatically filtered transcription of the speech, as dfxp
  or srt force-aligned timed subtitle files, and its json metadata.

&nbsp;&nbsp;&nbsp;&nbsp;`ep-asr.en.orig.<term>.<session_date>.<speech_id>.tr.verb.{dfxp,json,srt,txt}`  
&nbsp;&nbsp;&nbsp;&nbsp;[In train set] Automatically verbatimized transcription of the speech, as
  a txt transcription file, as dfxp or srt timed subtitle files,
  and its json metadata.

&nbsp;&nbsp;&nbsp;&nbsp;`ep-asr.en.orig.<term>.<session_date>.<speech_id>.tr.rev.{dfxp,json,srt,txt}`  
&nbsp;&nbsp;&nbsp;&nbsp;[In dev/test sets] Manually revised verbatim transcription of the speech,
  as a txt transcription file, as dfxp or srt timed subtitle
  files, and its json metadata.

Finally, in "refs" (only in "dev" and "test") each file contains every speech
in the corresponding dev or test set, that is, the full reference for that
set. In each case, we will find 4 files, containing the official non-verbatim
reference (`*.orig.*`) and the manually revised verbatim reference (`*.rev.*`), as
transcriptions (`*.ref`) and as segment time marked files (`*.stm`). In all 4
cases, the text is presented preprocessed for evaluation (tokenized,
lowercased, punctuation removed...).

#### Text data ("text" directories)

In the case of "train", they are subdivided in directories "external" and
"internal". "internal" contains all the official non-verbatim transcriptions
and translations in the train set, together with the selected non-overlapping
Europarl v10 transcriptions and translations; "external" contains the files to
make use of the external DCEP: Digital Corpus of the European Parliament.

Each "text" directory contains 2 subdirectories: "raw" (except in
"train/external"), "prepro" (in all sets), or "scripts" (only in
"train/external").

&nbsp;&nbsp;&nbsp;&nbsp;"raw" contains the raw text data for the corresponding set (`*.txt.gz`), and
  its metadata (`*.csv`). In the cases of "dev" and "test", both the official
  non-verbatim transcriptions (`*.orig.*`) and the manually revised verbatim
  transcriptions (`*.rev.*`) are included.

&nbsp;&nbsp;&nbsp;&nbsp;"prepro" contains the text data for the corresponding set, preprocessed for
  training or evaluation (tokenized, lowercased, punctuation removed...). This
  data is released to facilitate the reproducibility of our experiments.

&nbsp;&nbsp;&nbsp;&nbsp;Finally, "scripts" (only in "train/text/external") contains the script
  get_DCEP.sh, which can be used to download the DCEP corpus from its original
  website and save it in compressed plain text (`.txt.gz`).


EXTENDED DESCRIPTION
--------------------

Europarl-ASR (EN) is a large English-language speech and text corpus of
parliamentary debates for (streaming) ASR benchmarking and speech data
filtering/verbatimization, including 1300 hours of annotated English-language
speeches from European Parliament sessions held in the period 1996-2020.

It was compiled and released by the Machine Learning and Language Processing
(MLLP) research group of VRAIN Institut Valencià d'Investigació en
Intel·ligència Artificial, Universitat Politècnica de València
( [www.mllp.upv.es](https://www.mllp.upv.es) ).

Europarl-ASR (EN) includes:

#### Speech data

* 1263 hours of English-language annotated speech data (33,002 speeches, 1046
  speakers).
* 3 full sets of timed transcriptions: official non-verbatim transcriptions,
  automatically noise-filtered transcriptions and automatically verbatimized
  transcriptions.
* 17.5 hours of speech data with both manually revised verbatim transcriptions
  and official non-verbatim transcriptions, split in 2 independent
  validation-evaluation partitions for 2 realistic ASR tasks (with vs. without previous
  knowledge of the speaker).

#### Text data

* 69.4 million tokens of English-language text data.

#### Pretrained language models

* The Europarl-ASR English-language n-gram language model and vocabulary.

This data comprises most of the [European Parliament's English-language debate](https://www.europarl.europa.eu/plenary/en/debates-video.html)
recordings, transcriptions and translations available from the Parliament's
website from 1999 to 2020 (recordings being only available from 2008). This is
complemented by including all English-language transcriptions and translations
from the [Europarl](https://www.statmt.org/europarl/) v10 text corpus for the period 1996-1999.

Additionally, to increase text data for language modelling up to 170M tokens,
Europarl-ASR also includes tools to add all English-language text from the
[DCEP Digital Corpus of the European Parliament](https://ec.europa.eu/jrc/en/language-technologies/dcep).

Detailed dates of the EP speech and text data gathered:

* English speech: 2008-09-01 to 2020-05-27.
* English transcriptions: 1999-07-20 to 2020-05-27.
* Translations into English: 1999-07-20 to 2012-11-30.
* Europarl v10 (selected to avoid overlapping): 1996-04-15 to 1999-07-19.
* DCEP (does not include any EP reports of proceedings): 2001 to 2012.

For more information on the Europarl-ASR corpus and its creation, including
off-line and streaming ASR baselines, please refer to the Europarl-ASR
article (see "[CITATION](#citation)" above).


ACKNOWLEDGEMENTS
---------------

The authors would like to acknowledge:

* The European Parliament, the European Commission and other EU organizations,
  for making available a wealth of multilingual speech and text data, both in
  their websites and as ready-made corpora such as the DCEP Digital Corpus of
  the European Parliament
  ( https://ec.europa.eu/jrc/en/language-technologies ).

* Philipp Koehn for compiling the Europarl corpus
  ( https://www.statmt.org/europarl/ ).

This work has received funding from the EU's H2020 research and innovation
programme under grant agreements 761758 ([X5gon](https://cordis.europa.eu/project/id/761758)) and 952215 ([TAILOR](https://cordis.europa.eu/project/id/952215)); the
Government of Spain's research project [Multisub](https://www.mllp.upv.es/projects/multisub/) (RTI2018-094879-B-I00,
MCIU/AEI/FEDER,EU) and FPU scholarships FPU14/03981 and FPU18/04135; the
Generalitat Valenciana's research project [Classroom Activity Recognition](https://aplicat.upv.es/exploraupv/ficha-proyecto/proyecto/20190714)
(PROMETEO/2019/111) and predoctoral research scholarship ACIF/2017/055; and
the Universitat Politècnica de València's PAID-01-17 R&D support programme.


LEGAL DISCLAIMERS
-----------------

* Speech and text data from the European Parliament website (audio, official
  transcriptions and translations) were sourced from
  https://www.europarl.europa.eu/plenary/en/debates-video.html

* Text data from the DCEP Digital Corpus of the European Parliament are the
  exclusive property of the European Parliament. These data were sourced from
  https://ec.europa.eu/jrc/en/language-technologies/dcep (date of the latest
  update: 11 March 2015).


LICENCE
-------

* Speech and text data from the European Parliament website (audio, official
  transcriptions and translations) are the exclusive property of the European
  Union represented by the European Parliament. These data are reused here
  under the conditions stated in the European Parliament website's Legal
  notice ( https://www.europarl.europa.eu/legal-notice ).

* Text data from the DCEP Digital Corpus of the European Parliament are the
  exclusive property of the European Parliament. The European Parliament
  retains ownership of the data. These data are reused here under the usage
  conditions of the DCEP Digital Corpus of the European Parliament (
  https://ec.europa.eu/jrc/en/language-technologies/dcep#Usage%20Conditions ).

* Text data from the Europarl v10 corpus are reused here under the Europarl
  corpus terms of use ( https://www.statmt.org/europarl/ ).

* Europarl-ASR data and code not covered by the previously mentioned licences
  © 2021 Universitat Politècnica de València are licenced under CC BY 4.0. To
  view a copy of this licence, visit
  http://creativecommons.org/licenses/by/4.0/

See the [LICENSE](https://mllp.upv.es/git-pub/ggarces/Europarl-ASR/src/master/LICENSE) file for the full licence texts.
