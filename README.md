### Homework project 1주차 변경사항 공지
* 1주차 숙제의 마감은 6/10(토) 24:00 까지 입니다.
	* 2주차에 프로젝트를 완성시키는것을 목표로 합니다. 1주차에 다 끝낼 필요는 없습니다
	* 각 조별로 사정을 고려해서 1주차에는 각 조별 딱 1개의 commit 만 있으면 숙제 pass 로 인정합니다.
* 직접 merge 할 수 있게 권한을 주려 했는데, 프로젝트 참여 그룹이 적어서 직접 컨트롤 할 수 있겠네요.
	* 정석대로, PR 보내주시면 제가 merge 하겠습니다.
	* merge 가 늦어지면 메일 보내주세요.
* 최대한 실무에 가깝게 프로젝트를 진행해보려 합니다.
	* 특정 기능을 작업하기 전 github의 issue 에 작업내역을 등록해주세요. 같은 기능을 서로 다른조가 중복해서 개발하는 것 을 막기 위함입니다.
	* 등록양식은 제가 먼저 샘플로 등록했습니다.
	* issue 등록 -> 개발 -> PR -> review -> merge -> issue close  의 순서로 기능개발이 진행된다고 생각하시면 됩니다.
* 게시판 기능을 담당하는 조가 5개라 너무 많은 것 같습니다. 1개조는 덧글쪽으로 옮겨오시기를 부탁드립니다.

- - -

### Homework
* 게시판 기능 (16조) (14조) (12조) (10조) (11조)
	* 등록하기 (Robin)
	* 수정하기 (필수)
		* 자신이 등록한 글만 수정할 수 있습니다.
		* 게시글을 ID (PK) 가 바뀌어서는 안됩니다.  (Create 가 아니라 Update 가 이루어져야함)
	* 삭제하기 (필수)
		* 실제로 삭제하지 않고 isDel flag 를 두어 처리한다.
		* 자신이 등록한 게시글만 삭제한다.
	* 목록보기 (필수)
		* 페이징 기능이 있어야 한다. (Optional)
		* Title 로 검색이 가능해야 한다. (Optional)
	* 상세보기 (필수)
		* 삭제된 게시글을 조회할 수 없다.
	* 추천하기 / 반대하기 (Optional)
		* 한 사람당 하루 3번 추천 또는 반대 할 수 있습니다.

* 덧글 기능 (9조), (17조)
	* 등록하기 (필수)
		* 대댓글 개념이 있어야 한다.
	* 수정하기 (Optional)
		* 자신이 등록한 글만 수정할 수 있습니다.
	* 삭제하기 (Optional)
		* 자신이 등록한 글만 삭제할 수 있습니다.
	* 전체보기 (필수)
		* 대댓글 개념을 적용해야 함. (필수)
		* 대댓글의 개념을 위해 삭제된 댓글은 내용을 없애고 response 에 포함시켜야 합니다. (Optional)
		* sort 는 날짜별로 오름차순으로 하되, 대댓글은 상위댓글 바로 아래 나오도록 설정. (필수)
	* 추천하기 / 반대하기 (Optional)
		* 한 사람당 하루 5번 추천 또는 반대 할 수 있습니다.
		* 이 기능은 게시판의 추천하기와 독립적으로 사용됩니다.

* ~~MyPage 기능~~
	* ~~쪽지 기능~~
		* 발송하기 (필수)
			* 상대ID 로 쪽지를 보낼 수 있다.
			* 존재하지 않는 ID로 쪽지를 보낼경우 지정된 오류를 리턴한다.
		* 삭제하기 (Optional)
			* 보낸 쪽지와 받은 쪽지 모두 삭제할 수 있습니다.
			* 삭제는 여러개를 동시에 할 수 있다.
		* 목록보기 (필수)
			* 내가 받은 모든 쪽지 목록을 볼 수 있다.
			* 페이징 기능이 들어가야 한다. (Optional)
		* 상세보기 (필수)
			* 삭제한 쪽지는 조회할 수 없다.
		* 발신함 보기 (필수)
			* 내가 보낸 쪽지를 볼 수 있다. (필수)
			* 내가 보낸 쪽지를 상대가 읽었는지 확인할 수 있다. (필수)
			* 내가 보낸 쪽지를 읽기 전에 삭제할 경우, 당사자는 해당 쪽지를 볼 수 없다. (Optioanl)
		* 알림기능 (필수)
			* 읽지 않은 쪽지의 갯수를 보여준다.
* 커스텀 : 8조, 18조, 4조, (3조, 1조, 2조), 7조
	* 8조 : https://github.com/201302482/-TEAM8-Black_Jack
	* 7조 : https://github.com/dbrud951/five_poker
	* 4조 : https://github.com/seong954t/bot_project

* Local URL
	* http://localhost:8000/console
	* http://localhost:8000/swagger-ui.html
* 완료조건
	* 마감은 6/10(토) 18:00 까지로 정한다.
	* 상세 기능 대한 분배는 조별로 위임한다.
	* Priority 가 높은 기능을 우선적으로 구현한다.
	* Priority 가 낮은 기능은 코드에 주석으로 TODO로 마킹할 경우, 감점 없이 다음 주차 숙제에 포함시킨다.
	* 작업이 완료되면 직접 merge 한다. 컴파일 오류가 나타나건, Exception 이 발생하지 않는 상황이라면 merge 의 횟수에 대한 제약은 없다.
	* 잘 동작하던 코드에 오류가 발생하고 이를 강사가 알게 될 경우, 오류코드를 작성한 사람에게 email 및 trello 로 Noti 합니다.
	* 만약 Noti 후 1시간 이내에 응답이 없을 경우 감점 처리 합니다. (따라서 새벽에 merge 하는 것은 자제 바랍니다.)
	* 잘 모르는 내용은 google 및 강사에게 문의해 주세요. 최대한 친절히 답해드립니다.
* Git 사용방법
	* /napi/cnu-games-was 를 fork 따서 자신의 repository 로 가져온다.
	* 자신의 repository 에 있는 프로젝트를 clone 하여 local PC에 저장한다.
	* 자신의 PC에서 git remote add 명령으로 원본 프로젝트를 추가한다.
		```
		# upstream 이라는 이름으로 새로운 remote 저장소를 연결한다.
		git remote add upstream https://github.com/napi/cnu-games-was.git
		# remote 저장소를 조회한다.
		git remote -v
		```
	* 주기적으로 git pull upstream master 명령을 사용해서, upstream 과 싱크를 맞춰준다.
	* conflict 가 발생하는 경우, 직접 해결하도록 한다.
	* upstream 으로 PR은 누구나 날릴 수 있다. 각 조 조장에게 merge 권한을 부여하였으니, 조장에게 직접 merge 를 부탁한다.
	* <중요> PR을 날릴땐 항상 prefix 로 [X조] 를 붙여준다.
