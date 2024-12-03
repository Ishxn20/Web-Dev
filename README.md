# Web-Dev

`
# Check device availability (GPU/CPU)
print("CUDA Available:", torch.cuda.is_available())
DEVICE = torch.device("cuda" if torch.cuda.is_available() else "cpu")
# Model checkpoint and revision
CHECKPOINT = "microsoft/Florence-2-base-ft"
REVISION = 'refs/pr/6'
# Load Florence-2 base model and processor
model = AutoModelForCausalLM.from_pretrained(
CHECKPOINT, trust_remote_code=True, revision=REVISION).to(DEVICE)
processor = AutoProcessor.from_pretrained(
CHECKPOINT, trust_remote_code=True, revision=REVISION)
`
