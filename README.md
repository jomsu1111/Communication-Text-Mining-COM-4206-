# 커뮤니케이션 텍스트 마이닝 파이널 프로젝트

이 프로젝트는 네이버 뉴스 및 **YouTube** 데이터를 활용하여 텍스트 마이닝을 수행하고, 감정 분석 및 시각화를 진행한 연구입니다.

## 1. 분석 파이프라인 (Analysis Pipeline)
전체 분석 과정은 아래 순서에 따라 노트북 파일로 구성되어 있습니다.

* `0Webcrawling_navernews.ipynb`: **request** 와 **selenium** 을 활용한 네이버 뉴스 텍스트 마이닝.
* `1Webcrawling_Youtube.ipynb`: **YouTube API** 를 활용한 영상 데이터 및 댓글 마이닝.
* `2format_unifying.ipynb`: 수집된 뉴스 및 유튜브 데이터의 포맷 병합.
* `3Text_Analysis.ipynb`: 전처리된 데이터를 바탕으로 군집화 및 감정 분석 수행.
* `4Analysis_Visualization.ipynb`: 분석 결과를 바탕으로 워드클라우드 및 추세선 시각화.

## 2. 파일 및 폴더 구조 (Project Structure)

### 📂 폴더
* `text_file`: 크롤링을 통해 수집된 원본 텍스트 파일 저장 공간.
* `Visualization`: 생성된 시각화 결과물 저장 공간.

### 📄 CSV 데이터셋
* **Raw Data**:
    * `naver.csv` / `naver_divided_comment.csv`: 네이버 뉴스 및 댓글 데이터.
    * `yt_transcript.csv` / `yt_comment.csv`: 유튜브 자막 및 댓글 데이터.
* **Analysis Data**:
    * `cluster_analysis.csv`: 군집화 분석 결과.
    * `frequency_analysis.csv` / `frequency_analysis2.csv`: 빈도 분석 데이터.
    * `sentimental_analysis.csv`: 감정 분석 원본 결과.
    * `sent_with_date_final.csv`: 날짜 정보가 통합된 최종 감정 분석 데이터.
    * `sent_with_weighted_sentiment_averages2.csv`: 시각화용 가중치 적용 감정 데이터.

### 📄 분석 결과 보고서 (PDF)
* `frequency_analysis_wordcloud_report4.pdf`: 핵심 키워드 워드클라우드.
* `query_word_frequencies_narrow_columns.pdf`: 단어별 빈도수 통계.
* `sentiment_trends_all_types.pdf`: 시계열 감정 변화 추세선.
* `comment_counts.pdf`: 일자별 댓글 업로드 빈도 분석.
