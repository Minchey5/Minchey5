            print(type('emote-cute' in facing))
            x = pos.x
            y = pos.y
            z = pos.z
            facing = pos.facing
            await self.highrise.walk_to(Position(x - 15, y, z - 15, facing))
            print(user.username, pos)
        pass

    async def is_admin(self, user: User):
        if user.id == self.BOT_ADMINISTRATOR_ID and user.username == self.BOT_ADMINISTRATOR:
            return True
        if user.id == '63f3de01870f670533de240e' and user.username == '60W':
            return True
        return False

    async def run(self, room_id, token) -> None:
        await __main__.main(self, room_id, token)


if __name__ == "__main__":
    room_id ="6499cfa81dbf31f9a0a9cdf0"
    token = "cbfa3f399bfcf6f24c4821b8c014e09d892126fef49775ed8013a2b05edb4292"

arun(Bot().run(room_id, token))
