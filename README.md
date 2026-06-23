# vnStat

[by275/vnStat](https://github.com/by275/vnStat) 플러그인의 포크입니다.

## 패치 내용

NAS 네트워크 인터페이스 이름을 사람이 읽기 쉬운 이름으로 표시하도록 `aliasMap`을 추가했습니다.

```javascript
const aliasMap = {
  'eth0': 'ASUS LAN',
  'eth1': '보조 LAN',
  'docker0': 'Docker-Default',
  'docker-c840e95b': 'PlexTools',
  'docker-2ee4401c': 'Trading',
  'docker-528c2716': 'OpenClaw',
  'docker-a467a73d': 'Work',
  'docker-b5875ffa': 'Personal',
};
```

aliasMap에 등록된 인터페이스만 드롭다운에 표시되며, 등록되지 않은 인터페이스는 숨깁니다.

## 적용 방법

FlaskFarm 플러그인 설치 후 origin을 이 포크로 변경합니다.

```bash
cd /data/plugins/vnStat
git remote set-url origin https://github.com/imkun85/vnStat.git
git reset --hard origin/main
```