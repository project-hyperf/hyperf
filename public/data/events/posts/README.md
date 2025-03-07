# 사용법

## 게시물 추가는 posts 디렉토리에 마크다운 파일을 추가하면 됩니다.

- event : 미범주 이벤트와 관련된 내용
  > 해당 범주는 events/categories.json에 정의되어 있습니다.

## 파일의 첫 헤딩은 글의 제목으로 사용됩니다.

- 제목 이하 모든 내용은 콘텐츠로 렌더링됩니다.

## 파일의 첫 이미지는 썸네일로 사용됩니다.

## 이미지 삽입 시 주의

- 이미지는 /data 디렉토리로 시작하는 절대경로로 작성해야합니다.
  ex) `![이미지 alt](/data/events/posts/general/image.png)`

## 날짜 / 태그 / 장소

- 태그는 배열 안에 #과 함께 입력해주셔야 합니다.
  ex) ["#태그1", "#태그2"]

- 날짜, 장소는 **날짜**:, **장소**: 뒤에 입력해주세요.
  ex)
  **날짜**: 2024년 12월 12일
  **장소**: 장소

- 날짜를 입력하지 않으시면 작성된 날짜로 업로드 됩니다.
  태그와 장소는 선택 사항입니다.

## 게시물 추가 후 index.json에 파일명을 추가해야합니다.

- 파일리스트를 불러와 게시물 리스트를 렌더링하기 위해 사용됩니다.
- 실제 존재하는 파일명과 다르면 무시되니 유의해주세요.
- 배열에 존재하는 순서대로 게시물이 렌더링됩니다.

```JSON
//example
{
  "posts": [
    "first-post.md",
    "second-post.md",
    "some-directory/some-post.md"
    // 디렉토리명과 같이 작성해도 읽어올 수 있습니다.
    // 상대경로의 시작은 index.json이 위치한 디렉토리입니다.
  ]
}
```
