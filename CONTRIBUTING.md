# Contributing

Cam on vi muon dong gop! Day la huong dan chi tiet.

---

## Cach dong gop

### 1. Bao loi / De xuat

- [Open an issue](https://github.com/minhnv0807/fullstack-mkt-skills/issues/new/choose)
- Mo ta ro: Van de gi? Skill nao? Cai dat sao?
- Dinh kem screenshot / vi du neu co the

### 2. Cai tien skill hien co

```bash
# Fork repo → clone → tao branch
git checkout -b fix/ten-skill-van-de

# Sua SKILL.md
# Chay validator
./validate-skills.sh

# Commit theo Conventional Commits
git commit -m "fix(skill-name): fix benchmark number for beauty industry"

# Push va tao PR
```

### 3. Them skill moi

Skill moi phai co:
- **Foundation read:** Doc `product-marketing-context` truoc tien
- **Frontmatter day du:** name, description (trigger phrases!), metadata.version, category, related
- **4 cau thu thap thong tin** (toi da)
- **Core framework** voi bang bieu
- **Output template** co cau truc
- **Cross-references** den skill lien quan
- **Quality checklist**
- **Duoi 500 dong** (chi tiet day qua `references/`)

---

## Quy tac viet skill

### Frontmatter template

```yaml
---
name: ten-skill
description: "Khi nguoi dung ... [trigger phrases cu the]. Cung dung khi nguoi dung nhac 'A', 'B', 'C'. Skill nay ... [lam gi + ket qua]."
metadata:
  version: 1.0.0
  category: strategy | content | performance | operations | foundation
license: MIT
related:
  - skill-1
  - skill-2
---
```

**description quan trong:**
- 1-1024 ky tu
- Chua trigger phrases cu the (de AI nhan dien khi nao kich hoat)
- Mo ta dau ra (lam gi, ket qua gi)
- Tham chieu skill lien quan neu co

### Cau truc noi dung

```markdown
# Ten Skill

## Thu thap thong tin

### Buoc 0: Kiem tra context
Doc `.agents/product-marketing-context.md` neu co.

### Buoc 1: Hoi user (toi da 4 cau)
1. ...

## Nguyen tac cot loi
[Framework / Quy tac quan trong]

## Cau truc ket qua
[Template output voi bang bieu]

## Cross-references
[Skill lien quan va khi nao goi]

## Checklist chat luong
- [ ] ...
```

### Ngon ngu

- **Mac dinh: Tieng Viet** (khong dau hoac co dau deu duoc)
- **Thuat ngu chuyen mon:** Giu tieng Anh (ROAS, CPMess, UGC, TOFU/MOFU/BOFU)
- **Ngan gon, active voice**
- **Khong emoji** (tru khi user yeu cau)
- **So lieu: VN 2025-2026** — co trich dan `references/benchmarks-vietnam.md`

---

## Conventional Commits

```
<type>(<scope>): <description>

[body]
```

**Types:**
- `feat` — Them skill moi hoac tinh nang moi
- `fix` — Sua loi
- `docs` — Cap nhat documentation
- `refactor` — Restructure ma khong thay doi behavior
- `chore` — Cap nhat tool, config
- `test` — Them/sua test

**Vi du:**
```
feat(skill): add pricing-strategy skill
fix(03-danh-gia): correct CPMess TikTok benchmark
docs: update README install instructions
refactor: move references into per-skill folders
```

---

## Branch naming

- `feature/ten-skill-moi` — skill moi
- `fix/ten-skill-van-de` — sua loi
- `docs/phan-cap-nhat` — cap nhat doc
- `refactor/phan-restructure` — restructure

---

## PR Checklist

- [ ] Branch tu `master` moi nhat
- [ ] Chay `./validate-skills.sh` → khong co error
- [ ] Frontmatter du: name, description (trigger), version
- [ ] SKILL.md duoi 500 dong
- [ ] Co cross-reference den skill lien quan (neu applicable)
- [ ] Cap nhat `VERSIONS.md` voi version moi + ngay
- [ ] Cap nhat `.claude-plugin/marketplace.json` neu them skill moi
- [ ] Commit message theo Conventional Commits
- [ ] Mo ta PR day du: thay doi gi, ly do, anh huong

---

## Code review

PR se duoc review trong 3-5 ngay lam viec. Tieu chi:

1. **Tuan thu spec** — frontmatter, dung dinh dang
2. **Chat luong noi dung** — insight that, so lieu co nguon
3. **Vietnam-first** — benchmark VN, tranh copy paste nguoi nuoc ngoai
4. **Foundation integration** — co doc `product-marketing-context` truoc
5. **Cross-reference** — skill noi voi skill khac co hop ly

---

## Khong dong gop

- Skill "copy y chang tieng Anh" — khong gia tri cho thi truong VN
- Skill spam quang cao san pham/dich vu cua ban
- Noi dung vi pham thuan phong my tuc / quy dinh phap luat VN
- So lieu khong co nguon / bia dat

---

## Code of Conduct

Ton trong, xay dung, giup do. Khong ton cong, phan biet, thieu chuyen nghiep.

PR bi reject hoac issue bi close khong phai do tac gia — la do tieu chuan. Dung ngai hoi / thao luan.

---

## License

Dong gop cua ban se tu dong theo MIT License cua repo.
