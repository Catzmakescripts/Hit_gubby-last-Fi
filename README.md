getgenv().looping = true

task.spawn(function()
    while getgenv().looping do
        local args = {
            93.1362075805664,
            vector.create(-13.551054954528809, 3.293020486831665, -0.020241759717464447)
        }

        game:GetService("ReplicatedStorage")
            :WaitForChild("Networking")
            :WaitForChild("Server")
            :WaitForChild("RemoteEvents")
            :WaitForChild("DamageEvents")
            :WaitForChild("PhysicsDamage")
            :FireServer(unpack(args))

        task.wait(0.01) -- adjust delay if needed
    end
end)
