# GitHub Ation
https://github.com/Syota622/github_action_common

# featureからdevelopへmerge
- dev
1 $GITHUB_REF: refs/heads/develop
2 github.ref: refs/heads/develop
3 github.ref_name: develop
4 github.head_ref:
5 github.base_ref:
6 github.event_name: push
echo: dev

# developからmainへプルリクエスト
- stg
1 $GITHUB_REF: refs/pull/17/merge
2 github.ref: refs/pull/17/merge
3 github.ref_name: 17/merge
4 github.head_ref: develop
5 github.base_ref: main
6 github.event_name: pull_request
echo: stg

# 作成したプルリクエストの状態でdevelopへpush/merge
- dev
1 $GITHUB_REF: refs/heads/develop
2 github.ref: refs/heads/develop
3 github.ref_name: develop
4 github.head_ref:
5 github.base_ref:
6 github.event_name: push
echo: dev

- stg
1 $GITHUB_REF: refs/pull/17/merge
2 github.ref: refs/pull/17/merge
3 github.ref_name: 17/merge
4 github.head_ref: develop
5 github.base_ref: main
6 github.event_name: pull_request
echo: stg

# developからmainへマージ
1 $GITHUB_REF: refs/heads/main
2 github.ref: refs/heads/main
3 github.ref_name: main
4 github.head_ref:
5 github.base_ref:
6 github.event_name: push
echo: prod
